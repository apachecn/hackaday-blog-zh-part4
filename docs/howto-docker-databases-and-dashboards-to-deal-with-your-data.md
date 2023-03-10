# Howto: Docker、数据库和仪表板来处理您的数据

> 原文：<https://hackaday.com/2019/01/23/howto-docker-databases-and-dashboards-to-deal-with-your-data/>

所以你只是得到了一些类似 Arduino 或 Raspberry Pi 套件的东西，带有一些传感器。设置温度或运动传感器非常简单。但是你打算用这些数据做什么呢？在对任何人真正有用之前，它需要存储、分析和总结。你需要一个仪表板！

但是，即使在显示数据之前，您也需要将它存储在某个地方，这意味着数据库。你*可以*将你所有的数据发送到云中，并希望为你提供服务的公司背后有一个良好的商业模式，但坦率地说，即使是那些资金最雄厚、意图最好的公司的记录看起来也不太好。而且反正走最简单的路也学不到什么有用的东西。

相反，让我们采取第二简单的方法。这里有一个简短的教程，让你在 Raspberry Pi 上启动并运行数据库后端，并在你的笔记本电脑或手机上安装一个光滑的仪表板。我们将使用脚本和 Docker 来自动化尽可能多的事情。尽管如此，在这个过程中，你会学到一些关于 Python 和 Docker 的知识，但更重要的是，你将拥有一个自己的系统，可以进行扩展、定制，或者只是在家里进行试验。毕竟，如果“云”不让你摆弄他们的数据库，那会有多少乐趣呢？

## InfluxDB 和 Grafana 被包在 Docker 中

让我们把我们的零件放在一起，从数据库开始。InfluxDB 是一个开源的时间序列数据库，速度很快，旨在存储随时间变化的数据，比如你的传感器数据。它使用类似 SQL 的语言处理这些数据。编写 SQL 不是什么有趣的事情，但是它是标准的。

Grafana 是一个分析平台，可以让你可视化数据，并生成警报。它支持插件，这意味着它允许与其他软件集成。它将被用来与我们的 InfluxDB 对话，然后做一些很棒的事情。

Docker 是一个容器化的程序，这基本上意味着它允许我们把我们的应用程序，它的依赖关系，库和组件放在一个盒子里，这样我们就可以更容易地维护和移动东西。最重要的是，它允许我们使用别人已经准备好的容器，让我们的生活更轻松。

## 设置 Docker

现在我在 Linux 上做一些事情，因为我打算在完成实验后把它移植到树莓 Pi 上。也就是说，在命令行中键入几个句子就像浏览下拉菜单一样简单。第一步是安装 docker 和 docker-compose:

```

sudo apt-get update &amp;&amp; sudo apt-get install docker docker-compose

```

在这一点上没有太多其他的。重启你的机器以防万一。社区版的文档可以帮助回答您可能遇到的许多问题。

我们已经说过，docker 图像随时可用，因此我们需要一个用于 InfluxDB 的 docker 图像以及另一个用于 Grafana 的 docker 图像。为了快速启动和运行，从 [GitHub](https://github.com/inderpreet/py_docker_grafana_influxdb_dashboard) 中克隆我的库。

```

git clone https://github.com/inderpreet/py_docker_grafana_influxdb_dashboard.git
docker-compose up -d
chmod +x add_datasource.sh &amp;&amp; ./add_datasource.sh
cd pyclient &amp;&amp; chmod +x setup_env.sh &amp;&amp; ./setup_env.sh
python test.py

```

![](img/13af1065c6950ad94e94eb0decce2627.png)

为了测试工作是否正常，在一个新的终端上做一个`docker ps -a`。这应该会返回在您的系统上运行的容器列表。从列表中复制容器 ID 并运行`docker exec -it 1772a6e6387c influx`
来替换机器的容器 ID。您应该得到一个 influxDB shell，并可以运行如下命令:

`show users
show databases
create database hackaday`

我们需要创建一个数据库来存储我们的传感器读数，所以继续做吧。我用“hackaday”作为名字，虽然它可以是任何东西。

快速测试:

```
use hackaday
insert dummySensor v=123
insert dummySensor v=567
insert dummySensor v=000
select * from dummySensor

```

手动输入上述内容后，您应该能够看到时间序列中的数据。

![](img/de3d715be67bb80184c8423a0e356194.png)时间戳以纳秒为单位，一个特定系列可能有多个数据值，可能来自每个传感器。给定一些更好的名称，您可以使用下面的 SQL 查询查看任何给定传感器的数据:`select livingRoom from temperatureSensors`。注意:如果手动填充测试数据库，不要在逗号和下一个值字段之间添加空格。

我包含的 Python 脚本将生成一个指数形式的传感器数据，并在达到 100.0 时将该值重置为 1.1。这将允许我们在 Grafana 中绘制一条虚拟曲线。

## 设置 Grafana

Grafana 已经启动并运行了，这要感谢 docker，一旦你在浏览器中输入 URL，Grafana 就会出现一个登录提示。然后，您可以使用用户名/密码 admin/admin 登录。(你可能想尽快改变这一点！)

接下来，检查 Grafana 是否识别了您的 InfluxDB，如果没有，使用“添加源”。单击保存和测试并确认。确保选中顶部的默认复选框。

![](img/5a0bef967ecdb8c8ca7f7f53b96ac4c4.png)接下来，我们应该创建一个控制面板。从左侧菜单栏中，选择仪表板>主页和新仪表板。这应该会吐出一个带有几个图标的空画布。

选择图形，然后点击小标题称为面板标题或简单地按下键盘上的“e”。然后进行设置，以便:

–数据源设置为 InfluxDB
–选择测量设置为传感器数据
–填充设置为填充(先前)

在顶部，刷新设置为 5 秒，显示最近 15 分钟。

## 读数温度

我将 Python 脚本放在 Docker 容器之外的原因是，当我们进行必要的更改来读取传感器数据时，生活会更容易。现在，让我们从连接到微控制器的本地连接传感器接收数据，微控制器可以与计算机进行串行通信，由 Python 例程读取。

```
import serial

# replace with serial port name
ser = serial.Serial('/dev/ttyACM0')
ser.flushInput()

while True:
try:
temp_str = ser.readline()
temp = float(temp_str)
print(temp)
except:
print(&quot;Keyboard Interrupt&quot;)
break
```

只要你能让你的 Arduino 或等效物把数字吐出来作为一个字符串，这个脚本就会接收它们，并把它们翻译成浮点数。我将关于将数据推入 InfluxDB 的部分留给读者作为练习。(提示:您可以从/向我提供的`test.py`中复制和粘贴代码。)

## 树莓派和感官帽

下一步将是转向树莓派。圣诞节有吗？你很幸运。从 [GitHub](https://github.com/inderpreet/rpi_grafana_influxdb_python) 中克隆我的库，并执行与之前相同的步骤。代替`test.py`，我有一个可以执行的`sense_hat_temperature.py`。这样，您应该能够将传感器数据以及温度和湿度值添加到数据库中。

## 定制和结论

Docker 系统使用`docker-compose.yml`文件进行配置。特别是，有一个 volumes 变量创建了一个本地文件夹`influxdb_data`,数据就写在这个文件夹中。你可以把它配置成写一个外部驱动器，甚至是一个网络驱动器。

在树莓派的例子中，这非常有用。我希望有一种方法能够轻松显示传感器数据，同时进行一些 Python 和 Docker 实验。然而，这仅仅是开始，因为还有很多事情可以做。

到目前为止，我们的传感器设备是通过串行电缆连接到计算机的 Arduino。如果我们想无线传输，我们需要考虑将传感器的数据传输到数据库。在 ESP8266 上使用 MQTT 和 WiFi，你可以做得比[更糟。对于功率敏感的应用，](https://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)[考虑蓝牙 LE](https://hackaday.com/2018/08/03/beginning-ble-experiments-and-making-everything-better/) 。

现在，让这个系统启动并运行，用本地数据进行试验。这样，当您构建家庭传感和自动化网络的其余部分时，后端将为您做好准备。