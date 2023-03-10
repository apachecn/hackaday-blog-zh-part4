# 双节棍外壳中的自定义蓝牙操纵杆

> 原文：<https://hackaday.com/2020/04/26/custom-bluetooth-joystick-in-a-nunchuk-shell/>

凭借 Wii 独特的控制器，任天堂不仅为玩家提供了新的游戏体验，还为硬件黑客提供了一个仍然强劲的实验平台。一个恰当的例子是，由[Giliam de Carpentier]对第三方 Wii“Nunchuk”进行的修改，该修改将附件变成由 attin 44a 供电的独立无线控制器。

[![](img/2fe7a1eb869f5a5a1058585ad4809de9.png)](https://hackaday.com/wp-content/uploads/2020/04/avrchuk_detail2.jpg)

Milling a new home for the AVR

事实证明，双节棍盒内有相当大的空闲空间，所以[Giliam]发现添加新硬件并不像你想象的那么困难。当然，它有助于小型 SMD ATtiny44A 及其支持硬件安装在一个非常整洁的 PCB 上，该 PCB 连接到原始电路板的背面。

大多数其他硬件都以模块化组件的形式出现，如蓝牙发射器和 300 mAh 电池的 TP4056 充电控制器。在原来的双节棍线进入外壳的地方安装了一个微型 USB 充电端口，使整个事情看起来非常专业。

即使您对制作自己的控制器不感兴趣，[Giliam]在这篇文章中也涵盖了许多有趣的主题，例如处理不同的蓝牙连接方法和各种电源管理技术，以尽可能延长相对较小的电池的寿命。这不仅是一个引人入胜的阅读，而且是一个很好的例子，说明了完整的项目文档应该是什么样子。

在过去，我们已经看到了 Wii 双截棍的蓝牙转换，[但传统上，他们把原来的电子设备留在原地](https://hackaday.com/2011/02/18/bluetooth-enabled-wii-nunchuck/)。另一方面，我们也看到[的内部被像 Raspberry Pi Zero](https://hackaday.com/2019/05/13/wii-nunchuk-gets-a-built-in-raspberry-pi-zero/) 这样强大的东西所取代。

 [https://www.youtube.com/embed/iUegRV9EAMo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iUegRV9EAMo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

