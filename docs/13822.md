# 通过这个联网的猫砂盒追踪你的猫的体重

> 原文：<https://hackaday.com/2022/06/03/track-your-cats-weight-through-this-internet-connected-litter-box/>

随着猫肥胖率的上升，记录你的猫的体重是保持它们健康的重要部分。然而，称重环节可以是从日常工作到痛苦的过程，这取决于你的猫的性情。[Andy]的猫 Ellie 是那些不喜欢称重的人之一，所以为了不引人注目地跟踪她的体重，[Andy]发挥了创意，[为她的猫砂盒](https://andybradford.dev/2022/06/02/internet-of-poop-how-and-why-i-built-a-smart-litter-tray/)建造了一个联网称重平台。

该平台由两块 MDF 组成，两块 MDF 由两个称重传感器分开，称重传感器连接到 ESP8266。ESP 读取称重传感器，并通过其 WiFi 连接向 Adafruit IO 平台报告其发现，每当检测到使用垃圾箱时，就向[Andy]发送更新。猫的重量可以简单地通过从使用时测量的重量中减去未使用的猫砂盒的重量来计算。

[![A smartphone pop-up message from an IoT litter box](img/b2f7fb8fe5fcb9ac8bc698b32932e0fa.png)](https://hackaday.com/wp-content/uploads/2022/06/IoT-Litter-Box-Message.webp) 从称重传感器获得可靠的读数有点困难，因为当艾莉在垃圾箱周围移动时，测得的重量会剧烈波动。等待读数稳定下来，并使用超时来消除短暂移动的影响，这两种方法结合起来可以获得相当稳定的测量结果。分辨率甚至好到足以测量使用前后的垃圾重量差异。我们不确定知道你的猫每次拉多少屎有什么实际价值，但是如果数据在那里，你也可以记录下来。

[安迪]还想象了物联网垃圾箱的智能家居功能:例如，他可以运行空气净化器或在大量使用后发送 Roomba。这甚至不是我们展示的第一个联网的垃圾箱；我们已经看到[一个连接到 Thingspeak 平台](https://hackaday.com/2019/08/28/cat-litter-tray-joins-the-internet-of-things/)，以及[一个通过 Twitter](https://hackaday.com/2014/06/06/a-tweeting-litter-box/) 发送便便警报。如果你不在身边收拾残局，[一台自动抽油烟机可能会派上用场](https://hackaday.com/2008/09/16/hack-your-littler-box/)。

 [https://www.youtube.com/embed/fdV3rAeLJEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fdV3rAeLJEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

