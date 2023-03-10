# 无意排放

> 原文：<https://hackaday.com/2022/10/01/unintentional-emissions/>

首先，是 WiFi 路由器:[我的老式 WRT54G](https://en.wikipedia.org/wiki/Linksys_WRT54G_series) 给了我近二十年的服务。2.4 GHz 电路终于出了点问题，再也不能无线上网了。我的眼泪还没干，我们的温度计就出故障了。这是一种可以将温度传送到室内接收器的户外设备。在那之后，我们办公室灯的遥控器停止了工作，但是早就应该换电池了。

与此同时，我的妻子订购了一个新的室外温度计，它也很难保持连接。这年头品控！然后，我的 DIY 咖啡烘焙机无缘无故就火了一次。这个东西已经近乎可靠地工作了十年，我知道硬件和固件[就好像是我自己建造的一样](https://hackaday.com/2018/01/23/build-an-excellent-coffee-roaster-with-a-satisfyingly-low-price-tag/)——我自己的一个极其复杂的创造不可能有缺陷。(这是一个笑话，乡亲。)然后是最后一根稻草:办公室灯遥控器的电池测试良好。

我们绝对有一个闹鬼，一个无线电闹鬼。根本原因是 CMOS ICs 早期的一个老掉牙的问题——永远不要让输入悬空，它应该有一个确定的逻辑电平。让我解释一下。

WRT54G 是我自己的家庭自动化系统的中心，[一个 ESP8266 和其他设备的集合体，它们都可以愉快地相互交流 MQTT](https://hackaday.com/2019/11/07/found-footage-elliot-williams-talks-nexus-technologies/)。当它关闭时，没有一个小的 WiFi 节点能正确启动。其中一个[在这个视频](https://youtu.be/cAHWXy12c54?t=2019)中真实地描述了，是一个连接到 433 MHz 无线电发射机的 ESP8266。现在事情变得有趣了——温度计*和*,咖啡烘烤器*和*办公室的灯都运行在 433 MHz 上。

事情是这样的。WiFi-to-433 桥无法连接到 WiFi，并在初始化 GPIO 引脚的代码部分之前出错。433 MHz 发射机通电，但它的数字输入在微风中摇摆，导致它一直吐出随机数据，天线相当不错。这卡住了房子里的所有东西，很明显，甚至有一次，完全是出于偶然，他想到了打开咖啡烘烤器的命令。总之，拔掉桥就解决了一切。

这是一个有趣的故障诊断，因为它在不同的时间跨越了这么多不同的设备，有些是自制的，有些是商用的，而且都在不同的控制系统上。直到我把 433 MHz 上的所有东西都失灵放在一起，我甚至没有把它当成一个事件。然后，它变成了一个数字电子经典——悬空输入！

不管怎样，希望你玩得开心。并为不起眼的下拉电阻洒些铜。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!