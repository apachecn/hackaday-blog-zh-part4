# 一种使用通用模块的简单软功率开关

> 原文：<https://hackaday.com/2020/07/21/a-simple-soft-power-switch-using-common-modules/>

如果你想轻松控制电路中的功率，你可能会使用传统的拨动开关。虽然这肯定没有什么错，但物理开关在这一点上有点过时了。一个手指轻轻一点就能打开和关闭你的小玩意的软电源开关更符合 21 世纪的潮流。你可能认为这种现代的诡计在 DIY 项目中太难实现了，但是正如[马赛丽·卡拉诺维奇]，[所示，这实际上比你想象的要容易得多。](https://sasakaranovic.com/projects/3d-printer-enclosure-touch-control-for-your-light-setup/)

公平地说，这实际上不是他的目标。所有[马赛丽]试图做的就是想出一个巧妙的方法来控制他的 3D 打印机外壳中的 LED 照明。正如你在下面的视频中看到的，他做到了。但是他用来做这件事的拼凑电路可以很容易地用于其他电子项目。如果你正在使用 LM2596 DC-DC 转换器模块为你的小工具供电，你可以添加一个触摸感应软开关。

诀窍是利用 LM2596 上的使能引脚。常见的降压转换器模块将此引脚接地，因此调节器始终使能，但如果将此引脚从 PCB 上取下，并将其连接到 TTP223 电容式触摸传感器的输出，只需点击焊盘即可控制调节器。触摸传感器本身的电源来自调节器的输入端，因此即使下游断电，传感器仍处于唤醒状态，可以在需要时将芯片重新启动。

如果你对触摸控制不感兴趣，你可以尝试将调节器上的 enable 引脚连接到 ESP8266 上，然后[制作一个便宜的互联网控制的 DC 电源](https://hackaday.com/2019/12/26/new-part-day-sonoff-usb-smart-adaptor-taps-a-new-wifi-chip/)。

 [https://www.youtube.com/embed/6RUOkaM01S4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6RUOkaM01S4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

