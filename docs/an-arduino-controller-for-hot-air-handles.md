# 用于热风手柄的 Arduino 控制器

> 原文：<https://hackaday.com/2020/09/04/an-arduino-controller-for-hot-air-handles/>

总的来说，在过去十年左右的时间里，电子元件和用于摆弄它们的工具的成本一直在稳步下降。但是总会有一些寻找便宜货的黑客，他们希望得到更便宜的东西。典型的例子是热风返工站。你可以花 40 美元买到一个普通的 858D 工作站，但这并没有阻止[MakerBR]创造一个可以与其备用手柄一起使用的 Arduino 控制器。

[![](img/5e71815cc98ffa3be1192f7e418b90ad.png)](https://hackaday.com/wp-content/uploads/2020/08/ardu858d_detail2.jpg) 平心而论，价格似乎不是唯一的因素。毕竟，一个备用的 858D 手柄的价格大约是整个工作站的一半，所以在成本方面没有太大的改善空间。相反，[MakerBR]说 Arduino 版本的设计比普通硬件更高效、更可靠。

手柄连接器中的七根电线已经在之前的工作中绘制出来，尽管[MakerBR]确实需要验证所有东西都与提供的电路图匹配，因为一些供应商可能会篡改引脚排列。所有真正的魔法都发生在手柄本身，控制器只需要关注各种传感器，并为风扇和加热元件提供适当的控制信号。Arduino Pro Mini 可以胜任这项任务，定制的 PCB 可以让安装变得非常简单。

这不是我们第一次看到[有人更换这些入门级热气站](https://hackaday.com/2017/05/25/hack-your-hot-air-station/)的控制器，但因为有这么多不同的版本，你应该在打开你的并进行大脑移植之前做一些仔细的研究。

 [https://www.youtube.com/embed/L9gvOLftHnM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/L9gvOLftHnM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

