# USB 电源银行的自动关闭成为车库门遥控的有用功能

> 原文：<https://hackaday.com/2021/07/06/usb-power-banks-auto-off-becomes-useful-feature-in-garage-door-remote/>

对于那些只需短暂和偶尔使用的设备以及电池供电的设备来说，某种形式的节能是非常必要的功能。例如，当[PJ·艾伦] [将两个基于 ESP8266 的 NodeMCU 开发板变成一个替换的无线遥控车库门开启器](http://incredulist.blogspot.com/2020/10/garage-door-remote-2020.html)时，一个方便的 USB 电源组最终在将遥控器从工作台移开时充当了一个小骗子。PJ·艾伦没有将主板从 USB 转到电池供电，也没有实施某种睡眠模式或自动关机，而是简单地插入 USB 电源组，让它完成所有工作。

![](img/b56ea688afd976a078fcf194e351de33.png)

这是该功能的工作原理:一些 USB 电源组会自动关闭，除非它们检测到有意义的电流消耗。这意味着，如果电源银行正在给手机充电，它会一直开着，但如果它只是点亮了几个 led，它就会自动关闭。这个功能可能会令人沮丧，但[PJ·艾伦]意识到它实际上可以用于像他的车库门遥控器这样的设备。打开电源组会向 NodeMCU 板提供 5 V 电压并允许其工作，但大约 15 秒后，电源组会自动关闭。当然，将一个电源捆绑到遥控器上会使整个东西比它需要的更大，但这是一个非常聪明的使用最小负载作为一个毫不费力的自动关闭功能。

[PJ·艾伦]的 DIY 遥控器中的 NodeMCU 板使用 [ESP-NOW](https://www.espressif.com/en/products/software/esp-now/overview) 进行无线通信，这是一种来自 Espressif 的漂亮的无连接协议，我们已经看到它也被用于其他项目，例如[这种基于 ESP32 的对讲机](https://hackaday.com/2021/04/07/an-esp32-walkie-talkie-for-those-spy-radio-moments/)。