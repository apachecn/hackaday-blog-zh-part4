# ESP8266 动力油箱，带语音控制

> 原文：<https://hackaday.com/2018/09/06/esp8266-powered-tank-with-voice-control/>

(相对)低成本模块化组件的高可用性使得构建硬件比以往任何时候都更容易。取决于你想做什么，一个项目的硬件方面可能相当于黑客用乐高积木搭建。事实上，如果它真的和乐高积木有关，我们也不会感到惊讶。无论如何，简单快速的硬件构建为开发创意软件提供了更多的时间。最终结果是，我们开始看到非常复杂的系统被分解成易于复制的 DIY 构建，这在几年前几乎是不可能的。

[![](img/95677163b2c4b7625828e4ec0f9225e5.png)](https://hackaday.com/wp-content/uploads/2018/09/gvtank_detail.jpg)【igorfonseca 83】来信与我们分享他的模块化坦克平台，该平台使用 ESP8266 和一些软件黑客，允许用户从移动设备进行语音控制。作为 Hackaday.io 的一步一步的指南，这个项目非常适合互联网控制机器人的入门。无论你只是想尝试谷歌助手集成，还是用它作为一个空白的石板来引导一个远程控制的漫游者，这个项目都有很多东西可以提供。

底盘本身是一个商用套件，并且[igorfonseca83]使用 L298N 双通道 H 桥模块来控制其两个齿轮电机。一个 Wemos D1 充当操作的大脑，三个 18650 3.7V 电池提供电力以保持一切运转。有足够的扩展能力来添加传感器和其他设备，但对于这个项目来说，让它滚动是唯一的问题。

就软件而言，有许多部分协同工作来提供视频中演示的谷歌助手控件。首先是与 ESP8266 板 Adafruit 接口。IO，它连接到 IFTTT，最后是 Google Assistant。通过在 IFTTT 中设置几个由 Google Assistant 中的语音命令触发的两个可变短语，您可以通过 Adafruit.IO 将命令推回到 ESP8266。诚然，这是一个有点复杂的设置，但事实上涉及的编程很少，这对于不想陷入开发自己的互联网控制堆栈的所有细节的人来说是一个有趣的解决方案。

[igorfonseca83]对于建造遥控漫游车并不陌生。去年，我们报道了他的另一个作品，通过网络浏览器控制，并携带一部安卓手机来播放冒险视频。

 [https://www.youtube.com/embed/9Xa_xcF8h2s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9Xa_xcF8h2s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

