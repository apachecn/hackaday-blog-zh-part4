# ESP8266 交流控制器展示了一切可能

> 原文：<https://hackaday.com/2019/01/11/esp8266-ac-controller-shows-whats-possible/>

人们经常有这样的印象，即家庭制造的硬件注定会有某种业余的外观或感觉。这就好像只是因为你没有在商店里买它，它会看起来很便宜或扔在一起。虽然一个拼凑起来的设备*看起来确实像是由零件箱组装而成的(公平地说，有时确实如此)，但有很多 DIY 硬件的例子可以让商业产品物有所值。*

[![](img/398957580e59b62d01c8228e26b4b7ae.png)](https://hackaday.com/wp-content/uploads/2019/01/espac_detail.jpg) 一个很好的例子就是[这个由【Siti nut wai Sara】](https://maxmacstn.wordpress.com/2019/01/10/diy-wifi-ac-controller/)([Google Translate](https://translate.google.com.ar/translate?hl=&sl=th&tl=en&u=https%3A%2F%2Fmaxmacstn.wordpress.com%2F2019%2F01%2F10%2Fdiy-wifi-ac-controller%2F))创造的神奇的 ESP8266 空调控制器。在简单而优雅的 3D 打印外壳和有机发光二极管屏幕上非常光滑的用户界面之间，这个项目很容易成为一款商业设备。事实上，我们已经看到商业产品看起来没有一半好，更不用说在组件和打印机灯丝上提供相同的功能。这是一个完美的例子，说明了现代黑客或制造者利用我们目前可以获得的大量工具和组件能够做些什么。

也许这个项目最令人印象深刻的是，特别是考虑到它的外表看起来很好，它的内部实际上很少。除了 NodeMCU 板和 SSD1332 有机发光二极管显示器之外，该设备内部的唯一组件是三个触觉按钮、一个光敏电阻(因此它可以根据环境光水平调节显示器的亮度)、一个红外 LED(因此它可以向 AC 单元发送命令)和一些无源器件。这种设计的硬件方面非常简单，以至于[Sitinut]能够将整个东西放在一块 perfboard 上。并不是说当它被安装到 3D 打印的壁挂式外壳中，并配有打印的按钮帽时，你就能知道了。

虽然这个项目的硬件部分可能相当简单，但是软件却一点也不简单。[Sitinut]真的全力以赴为 ESP 编写代码，添加了一些小功能，如自动屏幕变暗和从 NTP 获取当前时间，这些功能在我们匆忙完成项目时经常被忽略。他甚至在有机发光二极管的屏幕上展示了一整套图标，这对销售这种专业外观大有帮助。但他的努力并不局限于化妆品或巧妙的功能，他还做了大量工作来解码用于控制 AC 单元的 IR 信号，并将所有功能和特性插入 MQTT。

我们已经看到了许多项目，[旨在将现有的暖通空调系统](https://hackaday.com/2017/10/03/drag-your-office-aircon-into-the-21st-century-with-wi-fi-control/)引入“物联网”[，有些项目远没有其他项目复杂](https://hackaday.com/2011/08/04/air-conditioner-regulation-using-a-hobby-servo/)。但是很少有人有[Sitinut]在他的控制器中所达到的完美水平，所以我们向他脱帽致敬。

 [https://www.youtube.com/embed/mG0bxod0GRU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mG0bxod0GRU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 BaldPower 的提示。]