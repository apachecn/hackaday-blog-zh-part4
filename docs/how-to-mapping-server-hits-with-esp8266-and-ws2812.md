# 如何:使用 ESP8266 和 WS2812 映射服务器点击

> 原文：<https://hackaday.com/2019/05/02/how-to-mapping-server-hits-with-esp8266-and-ws2812/>

为自定义数据可视化构建显示从未像现在这样简单。我刚刚为我的办公室完成了一个——作为一名安全研究员，我想要一个物理地图，显示我的服务器在地球上的哪个地方受到了攻击。但是同样的制造技术、硬件和网络资源可以用于任何其他目的。如果你是硬件新手，这是一个容易遵循的指南。如果你是服务器端代码的新手，也许你会发现它同样有趣。

我使用了一个 ESP8266 模块和一个通过 SSD1306 控制器连接的小型 128×32 像素有机发光二极管显示器。地图本身不需要非常精确，大致知道这个国家就足够了，因为它更多的是一个装饰而不是功能。这是一个很好的借口，可以把我的 5 米 WS2812B LED 灯条放在架子上使用。

![](img/c5c920e5eab5670ee08acb73bbd45b8a.png) [项目本身](https://github.com/kripthor/sitrepmap)大致可以分为 3 个部分:

1.  物理和硬件构建
2.  ESP8266 固件
3.  服务器端代码

这是一个相对简单的建筑，一个人可以在一个周末完成。它融合了 LED 灯条、ESP8266 wifi、有机发光二极管显示器、服务器端代码、python、geoip 定位、scapy 等等……你知道，有趣的东西。

## 硬件

首先，你需要一张地图。很明显，对吧？但是您的地图类型选择可能是项目的一个重要部分，可以极大地简化或复杂化整个设置。这里的问题是地图投影类型。有许多地图投影类型，其中一些比其他的更容易在这个项目中使用。理想的投影是等矩形投影，其中纬度和经度可以以线性方式映射。我用了中情局的时区地图[，因为，嗯，这有点酷。但这并不理想，因为它似乎是一个墨卡托投影变化(没有极点)，因此纬度增量并不是到处都一样，因为地图区域在极点附近被夸大了。](https://www.cia.gov/library/publications/the-world-factbook/graphics/ref_maps/physical/pdf/standard_time_zones_of_the_world.pdf)

![](img/b9b5dcfa3067d41182e5818255302b8e.png)

我用两张标准 A4 纸做了一张 50 厘米乘 24 厘米的地图。led 放在纸的后面，所以如果你想让灯真正突出，纸的厚度很重要。我有 5 米长、间距约为 16 毫米的 LED 条，我将其切割成 10 个单独的条。我将每条灯带的位置与 LED 灯的间距相匹配，这样我就有了一个完美的网格。这涵盖了整个经度范围和 65°到-35°之间的纬度。它并不完美，但可能覆盖了大约 95%的互联网连接世界。这是一种妥协。

我选择直接从电路板的 ESP8266 5V 引脚为 LED 灯供电，通过 USB 电缆供电。总共有 300 个发光二极管，我很确定，即使不算，它肯定不会工作。当我做原型的时候，我试了试，出乎意料的是，超过一半的 led 仍然亮着。我想，如果我需要所有的 led 都亮着，那我就有更大的问题要处理，因为那样我的服务器就会受到严重攻击！至少，我是这么告诉自己的，以此作为懒得加一个像样的电源(和更多的电线)的借口。如果你正在制作一个同时使用许多像素的显示器，你需要使用外部电源。

最后，我在地图上切了一个长方形的小洞，这样我就可以看到有机发光二极管屏幕上最近活跃的 4 个 IP 地址。它扼杀了一点复古风格，但好奇心占据了我最好的一面。这是在所有工作完成之后，所以这个洞看起来真的很糟糕。

**提示:** LED 灯带很棒，只有 3 根线，VCC、GND 和数据，每个像素都单独寻址。数据线也是有方向的，如果你要切割和焊接它们来制作电路板，小心不要改变数据线的方向。这样做将导致该条以及所有后续条停止工作。只是说，这并不是说我在第一次尝试时分心了… *(我是，我是…)*

## 固件

ESP8266 编程并不复杂。该设置初始化 WiFi、有机发光二极管和 LED 灯条。主循环定期对服务器进行池化，以获取最新的 IP 和地理位置，然后将该数据转换为特定的 LED，其颜色与服务器看到该 IP 地址后所经过的时间相关，就像热图一样。开始为红色，逐渐变为橙色、黄色、绿色和蓝色，直到 10 分钟后消失。

使用的 LED 条库是 [NeoPixelBus](https://github.com/Makuna/NeoPixelBus) ，值得一提的是![](img/f3c1233696045c5aceac81401ad972cd.png) ESP8266 有一些限制。ESP8266 需要硬件支持才能将数据发送到 LED 灯带。由于这一点以及每个硬件外设所用引脚的限制，我们唯一的选择是 GPIO1、GPIO2 或 GPIO3。最可靠的似乎是支持 DMA 操作的 GPIO3，不幸的是这也是 RDX0。此引脚的正常功能是串行接收，因此使用这种 DMA 方法不允许接收串行数据。对于这个项目，这不是一个问题，但值得注意。

使用的有机发光二极管库是 [Adafruit_SSD1306](https://github.com/adafruit/Adafruit_SSD1306) 。这个 ESP8266 模块文档不是很好，花了一些时间才弄清楚如何让它工作。“秘密”除了映射正确的 SDA、SCL 和 reset 线，就是在 初始化 Adafruit 库之前，调用 setup ***中的 Wire.begin()函数。***

```

#define OLED_RESET 4
#define OLED_SDA 2
#define OLED_SCL 14

void setup()
{
//OVERRIDE Wire.begin from Adafruit_SSD1306 to make this work on ESP8266 TTGO OLED
Wire.begin( OLED_SDA, OLED_SCL);
...

```

## 服务器端

服务器端代码是用 python 编写的，使用了 [python-geoip geolite2](https://pythonhosted.org/python-geoip/) 和 [scapy](https://scapy.net/) 库。Scapy 是一个非常棒的工具和库。如果你对网络测试感兴趣，特别是 pentesting，你可能知道它。如果你不是，Scapy 是 Philippe Biondi 用 Python 写的一个包操作工具。它可以伪造或解码数据包，在网络上发送它们，捕获它们，并匹配请求和回复。它还可以处理扫描、跟踪路由、探测、单元测试、攻击和网络发现等任务。Netcat 被称为“TCP/IP 瑞士军刀”, Scapy 就像它一样，但不是包。

要开始嗅探流量，您可以:

```

def custom_action(packet):
 srcip = packet[0][1].src
 gps = geolite2.lookup(srcip) ...

sniff(filter="ip", prn=custom_action, count=128)

```

这告诉 Scapy 嗅探 IP 流量，并对每个数据包运行自定义操作。在本例中，它将使用 geolite2 库来查找 IP。python-geoip-geolite2 包包括由 MaxMind 创建的 geolite2 数据，其使用非常简单。由于 GeoLite2 数据库是本地的，因此服务器不需要发出外部请求来识别 IP 位置。(也不是很准确，确实存在更好的选择)。过滤 IP 流量不足以识别攻击，合法流量也会出现。服务器是私有的，所以我们只能说它的很大一部分是“不想要的”流量。如果我们想更进一步，我们可以把地图和我们最喜欢的 NIDS 联系起来。但话说回来，这是一个周末项目…

我还使用了 [SimpleHTTPServer](https://docs.python.org/2/library/simplehttpserver.html) 包在一个自定义端口上设置了一个 web 服务器，这样 ESP8266 就可以连接到它并获取最新的结果，因为它们被定期写入一个文件。要使用 80 以外的端口，应该使用一个处理程序，如下所示:

```

Handler = SimpleHTTPServer.SimpleHTTPRequestHandler
httpd = SocketServer.TCPServer(("", PORT), Handler)
httpd.serve_forever()

```

这将在 port 创建一个 HTTP 开放端口，并为调用 python 代码的当前目录中的任何文件提供服务。当然，从安全角度来看，这并不十分安全。

## 结果呢

最后，我对结果很满意。我走了很多捷径和简化，但嘿，这是一个黑客。如果我有机会做版本 2 的话，会有很多地方需要改进，这很明显在我的脑海中，并且涉及到一整面墙。现在，你可以说，就精确度和分辨率而言，液晶显示屏显然要好得多。这是真的。但也许没那么有趣。我通常问自己如何才能做好 XYZ 项目，而不是为什么。这就是我如何结束充满东西的工作室和一堆，说实话，非常无用的项目。

我的收获是我从制作过程中获得的乐趣以及我在这个过程中学到的东西。这个还有一个闪光的奖励。这是大约 6 分钟(每帧 1 秒)的延时:

 [https://www.youtube.com/embed/bjHpIagEC3k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bjHpIagEC3k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我亲切地称中国为“永久的灯光秀”。固件和服务器端[的完整源代码可以在 GitHub、](https://github.com/kripthor/sitrepmap)找到，以防你想自己尝试并改进它。

如果这个项目不是你的事情，不要担心，我们[涵盖了](https://hackaday.com/2018/03/31/theres-more-to-midi-than-music-how-about-a-light-show/)很多[不同](https://hackaday.com/2018/03/28/an-led-effect-for-every-occasion/)和[有趣](https://hackaday.com/2011/12/03/10-meter-long-moving-light-show-is-mesmerizing/)其他[领条](https://hackaday.com/2016/02/14/controlling-rgb-leds-with-the-pi-zero/)项目在[过去也有](https://hackaday.com/2009/06/17/addressable-rgb-led-strip/)。