# 黑我的房子:UL 认证和用 ESP8266 开灯

> 原文：<https://hackaday.com/2019/04/22/hack-my-house-ul-certification-and-turning-the-lights-on-with-an-esp8266/>

很难想象没有智能照明的智能房子。也许这是懒惰，但是不用走到开关前就能开灯或关灯的能力是必须具备的，尤其是当腿上躺着一个熟睡的婴儿的时候。人们很容易在电气盒中塞进一个继电器，并用树莓 Pi 或微控制器 GPIO 来控制它们。虽然很诱人，但如果做错了，就会有真正的火灾隐患。更好的选择是其中一个集成的 WiFi 开关。Sonoff 可能是最知名的品牌，生产基于 ESP8266 的一系列设备。这些设备由市电供电，并通过 WiFi 连接到您的网络。Sonoff 设备的一个缺点是，它们只有在连接到 Sonoff 的云时才能工作。

被云提供商锁定的电灯开关是不可接受的。进入 [Tasmota](http://github.com/arendst/Sonoff-Tasmota) ，这是我们在之前已经介绍过的[。Tasmota 是一种开源固件，专门为 Sonoff 开关设计，但支持多种基于 ESP8266 的设备。Tasmota 不会连接到任何云提供商，除非你告诉它这样做，并且可以完全从本地网络控制。](http://hackaday.com/2019/03/21/old-wireless-switches-join-the-internet-of-things/)

## 认证、责任等等

我们熟知进口电子产品的一些缺陷，但是一个鲜为人知的问题是缺乏 T2 认证。在美国，有几个国家认可的测试实验室:保险商实验室(UL)和 Intertek (ETL)是最著名的。很多进口的电子设备，包括 Sonoff 设备，都没有这两个认证。这方面的问题是责任，万一发生最坏的情况，发生电气火灾。互联网上充斥着关于认证重要性的各种观点——缺失的认证标志介于毫无意义和完全危险之间。最常见的索赔是房屋火灾加上安装了未经认证的设备会导致保险公司拒绝支付。

我没有从网上重复这条明智的建议，而是向我的保险代理人询问了万一发生火灾时未经认证的设备。我发现保险机构避免给出明确的索赔支付答案。得到的回答是“视情况而定”:房主保险涵盖的是意外和突发事件。如果房主知道他们使用未经认证的设备，那么它可以被归类为“不是意外”。到目前为止，这个流言似乎是可信的。保险机构的最终答案是:非 UL 认证的设备可能会导致索赔被拒，但这取决于政策和其他细节——为什么要冒这个险呢？认证标志让保险公司更开心。

我也和我所在城市的电气检查员谈过这个问题。他评论说，未经认证的设备硬连线到房屋中是违反电气规范的。他重申了保险公司可以拒绝赔付的警告，但补充说，在受伤的情况下，可能会有更进一步的责任问题。我选择在家里使用经过认证的设备。你必须自己决定要用什么设备。

亚马逊上有一些设备声称拥有认证，但搜索认证数据库让我相信并非所有这些声明都是有效的。如果有疑问，有一个可搜索的 UL 数据库和一个可搜索的天祥数据库。

## 选择设备

所以，让我们回顾一下我们的要求:我们需要一个 WiFi 连接的交换机，由 Tasmota 支持，并要么 UL 或 ETL 上市。到目前为止，我已经找到了一个符合这些标准的设备。EtekCity ESWL01 经过 Intertek 认证，相对容易闪存到 Tasmota，甚至可以安装在 Decora 板上。我还收到确认，雪莉已经申请了 UL 认证，并期待着认证很快获得批准。一旦获得认证，他们也会做出很好的选择。

![](img/d13b472af848ebbdc71c5865136bc3d1.png)

使用 TTL 串行连接，闪烁开关相当简单。首先，在内部工作时，不要将开关连接到主电源。它可能会让你触电，这很糟糕，但更糟糕的是，很有可能会将电源电压馈入你的串行端口。相反，我们将使用串行适配器上的电源引脚为设备供电。注意，这不是一个 RS 232 串口，而是一个 3.3 V TTL 电平串行连接。我使用 MM232R 模块，但任何 TTL 串行适配器都可以，包括 Raspberry Pi。

要将设备置于闪烁模式，请在连接电源时将 GPIO0 短接至地。有几个闪存工具，但 Esptool 似乎是最简单的，只需一个命令即可进行闪存。官方建议备份出厂固件，将 ESP8266 清零，然后刷新固件。我觉得没有必要采取额外的步骤，但是如果你遇到问题，请记住。

```

esptool.py write_flash --flash_size 1MB --flash_mode dout 0x00000 sonoff.bin

```

我已经使用了发布的 Tasmota 二进制文件，但是如果你更喜欢自己编译它们，这里提供了说明。编译的一个好处是，你可以将你的 WiFi 信息和其他设置直接烘焙到二进制文件中。如果您不添加 WiFi 信息，该模块将广播您可以连接的开放 WiFi 网络，以便进行您的配置。设置您的 WiFi 信息，并确保选择一个有用的主机名，因为我们将使用它来控制交换机。

该设备将重新启动，并应连接到您的网络。最后一个配置步骤是告诉 Tasmota 它所运行的设备。我们将使用模板特性来定义重要的 GPIOs。

```

{"NAME":"EtekCityESWL01",
"GPIO":[255,255,255,255,52,53,255,255,255,21,122,255,255],
"FLAG":1,"BASE":18}

```

Tasmota 可以通过 web 界面、MQTT 或 REST API 进行控制，其中命令以 HTTP GET 和 HTTP POST 请求的形式发送。我们将使用这个 REST 接口。一旦开关闪烁并连接到您的 WiFi，请按照制造商的说明重新组装和安装。

## 触摸屏界面

我们将从构建一个简单的 PHP 控制接口`lights_api.php`开始。在隔离物联网网络时，这一额外的层非常重要，这意味着只需要一个 HTML 连接来控制一切。

```

<?php
  $curl_handle = curl_init();
  if ($_POST["toggle"]) {
    $command = explode(".", $_POST["toggle"]);
    curl_setopt( $curl_handle, CURLOPT_URL, 'http://' . $command[0] .
     '/cm?cmnd=' . $command[1] . '%20Toggle' );
    curl_exec( $curl_handle ); // Execute the request
  }
  if ($_GET["device"]) {
    curl_setopt( $curl_handle, CURLOPT_URL, 'http://' . $_GET['device'] .
     '/cm?cmnd=state' );
    curl_exec( $curl_handle ); // Execute the request
  }
  curl_close( $curl_handle );

```

这让我们可以发出一个简单的 HTML 请求，比如“lights_api.php？device=entry-light-1”，并接收一个带有设备当前状态的 JSON 对象。POST 消息允许切换开关状态。

你可能记得[我们使用树莓 Pi 触摸屏](https://hackaday.com/2019/02/27/hack-my-house-raspberry-pi-as-a-touchscreen-thermostat/)作为我们的主要界面之一。这个界面只有 800 x 480，这对于一个用户界面来说是相当大的设计挑战。我已经用 Libreoffice Draw 绘制了我房子的草图，并将其导出为 SVG。在这张图片上，我们将绘制图标来表示可控的灯光。

![](img/03b445cfe5444d56334c279e5b079698.png)

```

<div style="width:700px; margin:auto; margin-top: -4px;">

<div style="float:right; float:top;">
  <button onclick="window.location.href = 'index.php'" style="padding:25px 15px; margin-right:25px;">Thermostat</button>
 </div>

<div style="height:470px">
  <img style="position:absolute;" height=470px src="House-Blueprint.svg"/>
  <img class="light" style="position:absolute; margin-top:0px; margin-left:95px;" height=50px id="office-light-1.POWER3" onclick="button(this)" src="unlit.svg" />
  <img class="light" style="position:absolute; margin-top:15px; margin-left:30px;" height=50px id="office-light-1.POWER2" onclick="button(this)" src="unlit.svg" />
  <img class="light" style="position:absolute; margin-top:50px; margin-left:95px;" height=50px id="office-light-1.POWER1" onclick="button(this)" src="unlit.svg" />
  <img class="light" style="position:absolute; margin-top:225px; margin-left:155px;" height=50px id="entry-light-2.POWER" onclick="button(this)" src="unlit.svg" />
  <img class="light" style="position:absolute; margin-top:220px; margin-left:255px;" height=50px id="entry-light-1.POWER" onclick="button(this)" src="unlit.svg" />
 </div>

</div>

<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%3E%0A%20%20updateAll()%3B%0A%20%20let%20updateTimer%20%3D%20setInterval(updateAll%2C%2010000)%3B%0A%0A%20%20function%20button(caller)%20%7B%0A%20%20%20%20var%20xhttp%20%3D%20new%20XMLHttpRequest()%3B%0A%20%20%20%20xhttp.onreadystatechange%20%3D%20function()%20%7B%0A%20%20%20%20%20%20update(caller)%3B%0A%20%20%20%20%7D%0A%20%20%20%20xhttp.open(%22POST%22%2C%20%22lights_api.php%22%2C%20true)%3B%0A%20%20%20%20xhttp.setRequestHeader(%22Content-type%22%2C%20%22application%2Fx-www-form-urlencoded%22)%3B%0A%20%20%20%20xhttp.send(%22toggle%3D%22%20%2B%20caller.id)%3B%0A%20%20%7D%0A%0A%20%20function%20update(element)%20%7B%0A%20%20%20%20var%20switchInfo%20%3D%20element.id.split(%22.%22)%3B%0A%20%20%20%20var%20xhttp%20%3D%20new%20XMLHttpRequest()%3B%0A%20%20%20%20xhttp.onreadystatechange%20%3D%20function()%20%7B%0A%20%20%20%20%20%20if%20(this.readyState%20%3D%3D%204%20%26%26%20this.status%20%3D%3D%20200)%20%7B%0A%20%20%20%20%20%20%20%20var%20state%20%3D%20JSON.parse(this.responseText)%3B%0A%20%20%20%20%20%20%20%20if%20(state%5BswitchInfo%5B1%5D%5D%20%3D%3D%20%22ON%22)%20%7B%0A%20%20%20%20%20%20%20%20%20%20element.src%20%3D%20%22lit.svg%22%3B%0A%20%20%20%20%20%20%20%20%7D%20else%20%7B%0A%20%20%20%20%20%20%20%20%20%20element.src%20%3D%20%22unlit.svg%22%3B%0A%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%3B%0A%20%20%20%20xhttp.open(%22GET%22%2C%20%22lights_api.php%3Fdevice%3D%22%20%2B%20switchInfo%5B0%5D%2C%20true)%3B%0A%20%20%20%20xhttp.send()%3B%0A%20%20%7D%0A%0A%20%20function%20updateAll()%20%7B%0A%20%20%20%20document.querySelectorAll('.light').forEach(function(light_element)%20%7B%0A%20%20%20%20%20%20update(light_element)%3B%0A%20%20%20%20%7D)%3B%0A%20%20%7D%0A%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" />

```

这里有一点诡计。img 元素包含每个交换机的完整定义。`updateAll()`函数遍历类“light”的所有元素，获取每个开关的状态并更新图形。每个 img 的 ID 包含交换机的主机名，以及我们感兴趣的 GPIO 的指示器，允许支持控制多个灯的设备。在每个 img 元素上运行`update()`函数，使用 ID 中的信息从我们的 PHP 接口请求开关状态。

我们还定义了每个 img 的`onclick`，为我们提供了触摸屏功能。发送触发请求后，我们还强制更新那个灯，以保持接口同步。我将把它作为一个练习，让读者用 PHP 写出 img 元素并添加一个数据库后端。

这样，我们就有了一个简单的触摸屏界面来控制照明。它可以在手机或桌面上工作，所以不用再吵醒宝宝关灯了。这也是进一步编程的一个简单接口。希望前门打开时走廊灯亮起？只需在处理程序脚本中添加一个 HTTP GET 请求。

每个房间都有一个树莓派，灯光也得到控制，我在智能房子方面有了一个良好的开端。我的愿望清单上还剩下一些项目，但是我想听听你的意见。我还没有介绍什么你认为不可或缺的智能家居功能？