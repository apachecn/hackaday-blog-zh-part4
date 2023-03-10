# 无线时代有线的优势

> 原文：<https://hackaday.com/2022/04/09/the-virtue-of-wires-in-the-age-of-wireless/>

本周我们发表了一篇关于 RS-485 的文章，这是一种抗噪声差分串行多点总线架构。(告诉我你还会去哪里看那样的文章！)在过去，我已经享受过 RS-485 的乐趣，阅读这篇文章让我想起了那些日子。

你看，RS-485 可以让你把一大堆设备连接到一束 Cat5 电缆上，如果你把它和 [Modbus 协议](https://en.wikipedia.org/wiki/Modbus)结合起来，你就可以让它们在一个网络中一起工作。将其中的几条 Cat5 线路用于供电，这是家庭或黑客空间小型设备网络的完美配方——这是你和我今天使用 WiFi 和 ESP8266 所做的事情。

有线更可靠，移动部件更少，可以解决“我如何给这些东西供电”的问题。它本质上更简单:没有无线电，只有串行数据作为电线上的电压运行。但是没有人喜欢铺设电缆，而且 ESP 解决方案的演示代码太多了。不可否认的是，WiFi 的开发和跨设备兼容性非常容易。您的设备可以直接与计算机或整个互联网对话。这就是《连线》的死亡。

尽管如此，我还是有些钦佩有线总线的专用简单性和防爆特性。这感觉有点复古，但也许我会拿出一些旧的 Cat5，在办公室里放着它，只是为了怀念过去的时光。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!