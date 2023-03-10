# LED 时钟展示了它的管道

> 原文：<https://hackaday.com/2022/09/19/led-clock-has-its-pipes-on-display/>

对于大多数黑客和制造者来说，建造一个时钟是一种成年礼。然而，很少有人会像[TerraG2]的这个设计一样与众不同和引人入胜。

通过结合可寻址 led、光导管和 7 段显示屏，[TerraG2]打造出了一款外观精美的时计，必将成为一个绝佳的谈话开场白。它充满了各种功能，如自动亮度控制、加速度计控制的用户界面和 WiFi，以确保它始终准确无误。

![partial rear view of the clock showing illuminated light pipes](img/32e18e662456a8f0094b90901ca85f89.png)

Partial rear view of the clock showing illuminated light pipes

将光导管留在主显示器后面的决定确实使该项目从其他时钟构建中脱颖而出，而[TerraG2]用来实现这种外观的方法无疑将可转移到其他项目中。

led 由标准的 8×8 RGB 矩阵提供，带有定制的 3D 打印护罩来固定光导管，另一端有一个智能连接器来照亮各个部分。每段两个发光二极管，每位七个发光二极管，四个数字，如果你能想到这八个备用发光二极管的用途，甚至还有空间来实现一些额外的功能。

该项目的大脑是一个带有 MPU6050 惯性测量单元(IMU)的 ESP8266 D1，用于检测它何时翻转以改变配色方案。

完整的[文档在 Github](https://github.com/terra819/LightPipesClock) 上，正在使用的时钟的视频在休息之后。

在我们看到的其他一些时钟项目中，光导管也发挥了巨大的作用，比如这个[现代谢妮时钟](https://hackaday.com/2016/12/22/light-pipes-and-leds-team-up-for-a-modern-take-on-the-nixie-tube/)和这个[“时钟之钟”](https://hackaday.com/2021/03/19/clock-of-clocks-adds-light-pipe-hands-for-beauty-and-function/)，以及我们最近展示的这个[光器官](https://hackaday.com/2015/07/22/led-organ-chimes-its-light-pipes/)。

 [https://www.youtube.com/embed/2n5Elx5SJpc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2n5Elx5SJpc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

