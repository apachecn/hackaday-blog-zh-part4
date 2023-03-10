# DIY 六通道 Arduino 遥控发射器

> 原文：<https://hackaday.com/2019/03/19/diy-six-channel-arduino-rc-transmitter/>

就在不久前，遥控发射器，至少是值得拥有的，还是昂贵的装备。甚至在最近，RC 发射器运行开源固件的想法还被认为是白日梦。然而，今天购买廉价的进口发射机和闪存社区开发的固件(如果它没有预装)是常见的地方。毫不夸张地说，我们目前正处于业余爱好遥控发射器的“黄金时代”。

但是如果运行可定制软件的廉价硬件还不够呢？如果你想更进一步呢？在这种情况下， [[Electronoobs]有一个 Arduino 供电的 RC 发射器，上面有你的名字](https://www.electronoobs.com/eng_arduino_tut86.php)。但这不是一块上面有几个廉价操纵杆的原型板，尽管他也做了一个。这个版本的目标是在业余爱好者的能力范围内，让它看起来和执行起来尽可能的专业。最终产品可能不会赢得任何设计奖项，但它仍然是一个令人印象深刻的演示，说明了个人黑客和制造商今天可以利用我们可以获得的令人难以置信的技术实现什么。

[![](img/c36f9f3affbc702abb29a13c689fa9fd.png)](https://hackaday.com/wp-content/uploads/2019/03/ardutx_detail.jpg) 那么这个自制的无线电控制系统是怎么回事呢？在背板[electronio OBS]内部安装了电池、充电模块和电压调节器，该电压调节器将电池电压降低到驱动发射器其余电子设备所需的 3.3 V。另一方面，有一个 Arduino Nano，一个 NRF24 模块和一个有机发光二极管显示器。最后，我们有各种开关、按钮、电位计和两个非常漂亮的 JH-D202X-R2 操纵杆供用户输入。

正如你可能已经猜到的，建造你自己的发射机也意味着建造你自己的接收机。不幸的是，你无法将你现有的遥控车辆绑定到这个无线电上，但由于接收器端不比另一个 Arduino Nano 和 NRF24 模块复杂，如果你愿意，改造它们应该不难。

低成本消费类 [RC 发射器可能是一个大杂烩](https://hackaday.com/2018/03/27/terrible-rc-transmitter-made-less-terrible/)。有一些[令人惊讶的体面的选择在那里](https://hackaday.com/2018/02/26/quantifying-latency-in-cheap-rc-transmitters/)，但这并不奇怪，黑客们[有兴趣只是旋转他们自己的版本](https://hackaday.com/2019/01/15/arduino-rc-transmitter-for-homebrew-projects/)。

 [https://www.youtube.com/embed/YMF5NXeHOnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YMF5NXeHOnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

