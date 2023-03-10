# Linux Throwie:一颗非航天卫星

> 原文：<https://hackaday.com/2018/11/20/the-linux-throwie-a-non-spacefaring-satellite/>

投掷器在硬件文化中占据着特殊的位置——一个硬币电池、LED 和一块磁铁，可以被扔进一个无法到达的地方，并作为一个彩色光的小灯塔贴在那里。我们中的许多人会深情地记得这是第一个项目。唉，时间不可避免地在前进，发出欢快的灯光不再教会我新的技能。出于对那些简单时代的认可，我一直致力于构建一个功能齐全的服务器的不同寻常的想法，这种服务器可以放在偏远的地方并保持功能，就像一个投掷器(请不要真的扔了它)。它有点古怪，但如果你把它放在有阳光的地方，它仍然可以偶尔远程访问几年。

![](img/814cfbdfe7585ab131c31aab34ae8ae3.png)

不久前，我描述了这个太阳能驱动的云可访问 Linux 服务器的能量阶段。它只在需要时激活，所以一个小的太阳能电池和适度的电池就足以维持整个节目的运行。

在我们停下来的地方，我有一个太阳能电池，可以给电池充电，并提供稳定的 12 V 和 5 V 输出。为了使其成为功能性设备，需要解决三个高级问题:

1.  必须能够在没有直接物理接触的情况下设置设备
2.  您必须能够根据需要远程打开和关闭它。
3.  它需要可以从互联网上访问。

有趣的是，这个硬件让我想起了卫星。当然，它不是要去太空，但我确实计划把它放在一个不容易再次到达的地方，它依靠太阳能供电，有一个特殊的子系统(ESP8266)来管理电源，检查远程激活，并根据需要打开和关闭主计算机(Raspberry Pi 3)。这听起来很像太空竞赛技术，对吗？

由于今天我有比平时多一点的代码要与大家分享，所以我将讨论最有趣的部分，并在文章结尾提供完整固件文件的链接。

## 设备设置

设备设置是一个很好的起点，它有两个组件:Raspberry Pi 3 上的操作系统(在这里是 Raspbian Stretch Lite)，以及控制 Raspberry Pi 3 是打开还是关闭的低功耗系统。在这两种情况下，我们通过扫描具有已知 SSID 的无线网络(比如从您的移动电话)来处理这个问题。

在 Raspbian 中，这相当容易——我们打开/etc/network/interfaces，并将配置网络的优先级设置为一个较高的数字:

```

network={
ssid = &quot;setup network name&quot;
psk = &quot;setup network password&quot;
priority = 999
}

```

对于我们的电源控制硬件，NodeMCU 中有一个名为“[最终用户设置](http://nodemcu.readthedocs.io/en/master/en/modules/enduser-setup/)的模块，允许您远程连接到 ESP8266，扫描网络，并连接到其中一个网络，保存凭据。当某个热点在范围内时，我们需要做的就是有选择地运行包含它的程序:

```

function listap()
dofile('setup.lua')
end

scan_cfg = {}
scan_cfg.ssid = &quot;setup network name&quot;
scan_cfg.show_hidden = 1
wifi.sta.getap(scan_cfg, 1, listap)

```

然后在 setup.lua 中，我们运行最终用户设置。这导致 ESP8266 充当名为“SetupGadget”的热点，后跟几个十六进制数字:

```

enduser_setup.start(
function()
print(&quot;Connected to wifi as:&quot; .. wifi.sta.getip())
end,
function(err, str)
print(&quot;enduser_setup: Err #&quot; .. err .. &quot;: &quot; .. str)
end
)

tmr.alarm(1,1000, 1, function() if wifi.sta.getip()==nil then print(&quot; Wait for IP address!&quot;) else print(&quot;New IP address is &quot;..wifi.sta.getip()) tmr.stop(1) node.dsleep(2000000) end end)

```

通过这种设置，我们可以将服务器和控制硬件连接到新的无线网络，而无需直接物理访问。太阳能需要光，这可能会在我的屋顶上，我不喜欢在我需要重置我家 WiFi 密码的任何时候爬上去取它。如果你有一个非常高的屋顶，给自己造一个[定向波导天线](http://hackaday.com/2009/07/07/various-cantenna-builds/)——我已经能够通过几个混凝土建筑以这种方式获得超过 100 米的范围。还有 Brian Benchoff 的 [3D 打印 ESP8266 碟形天线](https://hackaday.com/2017/01/30/increase-the-range-of-an-esp8266-with-duct-tape/)。

## 远程电源控制

接下来，我们需要能够远程打开或关闭服务器。我们将使用 MQTT 来实现这一点，MQTT 指向一个解析为云 VPS 的域名。在 VPS 上，您唯一需要的是 mosquito MQTT 代理，因此没有必要为高端服务器付费。请注意，这里有一些方法可以[实现一些基本的安全性](http://hackaday.com/2017/06/20/practical-iot-cryptography-on-the-espressif-esp8266/)，但是为了简洁起见，我将把它作为一个练习留给您自己去探索。

请注意，我们的硬件只是偶尔活动——我将它设置为每 15 分钟左右唤醒一次，以检查 MQTT 代理。为了确保收到消息，发送方需要在发送激活命令时设置“保留”标志。这保证了当 ESP8266 唤醒并检查新消息时，该消息将在那里，只要我们不使用一些其他保留的消息来替换它。domain.com MQTT 代理的 Python 简短示例，主题为 solarserver:

```

import paho.mqtt.client as mqtt #import the client
broker_address=&quot;domain.com&quot;
client = mqtt.Client(&quot;P1&quot;) #create new instance
client.connect(broker_address, port=1883) #connect to broker
client.publish(&quot;solarserver&quot;, payload=&quot;activate&quot;, qos=0, retain=True)

```

在我们的 ESP8266 上，我们检查命令“activate ”,然后运行一个程序来打开 Raspberry Pi 3:

```

ClientID = 'Node001'
m = mqtt.Client(ClientID, 120)

m:connect(&quot;domain.com&quot;, 1883, 0, function(client)
print(&quot;connected&quot;)
client:subscribe(&quot;/solarserver&quot;, 0, function(client) print(&quot;subscribe success&quot;) end)
end)

m:on(&quot;message&quot;, function(client, topic, data)
print(topic .. &quot;:&quot; )
if data ~= nil then
print(data)
if data == &quot;activate&quot; then
dofile('active.lua')
m:close()
end

end
end)

```

程序“active.lua”将 GPIO 拉高，以启用连接到 Raspberry Pi 3 的 5v 线路，并监控电池电压。如果电池电压降得太低，或者收到关机命令，就会断电(先关机是个好主意)。

## 深入挖掘 SSH 隧道

但是，如果我们可以打开设备却不能使用它，这对我们有什么好处呢？当我计划移动这个设备进行软件演示时，如果我不用太担心防火墙、路由器和它可能带来的其他麻烦，那就太好了。这是我们探索[反向 SSH 隧道](http://raymii.org/s/tutorials/Autossh_persistent_tunnels.html)的地方。

通常，您会建立一个 SSH 连接，因为您想要对远程机器进行安全的 shell 访问，并且拥有一个证书或用户名+密码对以及机器的地址。在这种情况下，客户端的地址及其网络状态(其背后的路由器等)通常并不重要，但假设服务器的地址是已知的，并且所有端口转发和防火墙设置都配置为接受流量。

在反向 SSH 连接中，服务器启动到客户端的连接，该连接用于允许客户端连接回服务器。在启动从服务器到客户机的连接时，需要指定一个端口。当登录到客户端时，您使用 SSH 在该端口上登录到 localhost，流量将被发送到服务器，从而允许您登录。

我们需要将这个过程自动化，这样它才会有用。第一步是在您的 VPS 上创建一个访问受限的用户(本例中为 your_username)。我们的服务器会自动登录到它，如果你有任何远程价值的东西，用 root 帐户登录可能是个糟糕的主意。记下这个新用户的密码。

接下来，我们启动 Raspberry Pi 3(我们假设您在这里使用 Raspbian Lite)，设置一个新的 root 密码，安装 autossh 来管理连接，创建一个带有证书的新用户(与 VPS 用户同名)，最后使用 SSH-copy-id 将该证书[复制到我们的 VPS:](http://hackaday.com/2017/02/05/grant-anyone-temporary-permissions-to-your-computer-with-ssh/)

```

$apt-get install autossh
$useradd -m -s /bin/bash your_username
$su – your_username
$ssh-keygen -t ed25519
$ssh-copy-id your_username@(VPS IP address) -p 22

```

然后，我们运行 raspi-config 来启用 SSH 服务器，并让该用户在启动时自动登录。现在，我们设置使用证书而不是用户名+密码对通过 SSH 登录我们的 VPS，这更容易实现自动化。让我们从我们的 Raspberry Pi 3 建立一个反向 SSH 隧道来测试它:

```

$autossh -M 0 your_username@(VPS IP address) -p 22 -N -R 8081:localhost:22 -vvv

```

如果成功，您应该能够通过以下命令从 VPS 建立到 Raspberry Pi 的 SSH 连接:

```

$ssh your_username@localhost -p 8081

```

假设工作正常，我们继续创建一个服务，在网络接口启动几秒钟后建立连接。我们将使用 [systemctl](http://www.tecmint.com/manage-services-using-systemd-and-systemctl-in-linux/) 来完成这项工作，但是首先我们需要创建一个简短的 shell 脚本供 systemctl 调用。创建一个文件 autossh.sh，使其可执行(例如，使用 chmod)，并使用以下内容填充它:

```

sleep 15
autossh -M 0 your_username@(VPS IP address) -p 22 -N -R 8081:localhost:22 -vvv

```

“睡眠 15”会在网络接口启动后等待 15 秒。没有这个，我发现脚本运行得有点太早，我不能解析 VPS 主机。有更好的方法来解决这个问题，但是这是最简单的。现在，我们创建运行该脚本的服务，使用:

```

$systemctl edit --force --full autoautossh.service

```

然后，我们输入以下内容，然后保存文件:

```

[Unit]
Description=My Script Service
Wants=network-online.target
After=network-online.target

[Service]
Type=simple
User=pi
WorkingDirectory=/home/your_username
ExecStart=/bin/bash /home/your_username/autossh.sh

[Install]
WantedBy=multi-user.target

```

然后我们启用并测试它。在第二个命令之后，反向 SSH 隧道应该可以运行了，您可以尝试一下——如果现在不工作，它在引导时也不会工作:

```

$systemctl enable autoautossh.service
$systemctl start autoautossh.service

```

如果您现在可以访问，那么它应该会在引导后自动建立反向 SSH 隧道，如果它被破坏，还会自动重新建立。如果你有网络连接不良的问题，你可以研究一下作为 SSH 替代方案的 Mosh。

![](img/b78456616196556b04ea35e364966422.png)

The case should probably be white, given that it’s going to be sitting in the sun a lot. Two solar panels fit nicely, so now it uses 0.6W of solar panels. Hot glue is to fill the small gap between the panels and the case, and for cosmetic effect, of course.

至此，您差不多完成了:只需将您的功率级的 5 V 输出插入您的 Raspberry Pi，并将其放入一个防风雨的盒子中。当您向 MQTT 主题发送保留消息“activate”时，服务器将在大约 15 分钟内打开。我建议测试它，并听一会儿 MQTT 主题，以确保它像预期的那样工作，这样您就可以知道电池可以持续多长时间。

按照承诺，这里是[完整固件源代码](http://github.com/seanboyce/remote-execution)。仔细阅读，并在下面的评论区留下你的任何问题。我也很想知道你会用 Linux 投掷器做什么？