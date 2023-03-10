# 拍摄电子邮件以获得拍摄机会

> 原文：<https://hackaday.com/2022/10/17/shoot-an-email-to-get-a-shot/>

[_Pegor]想为他们的朋友的生日创造一个倒酒机。不幸的是，构建没有及时完成，但至少现在 JagerMachine 已经完成，其他人可以使用它了。

JagerMachine 有一个[蠕动泵](https://hackaday.com/2022/01/12/stout-peristaltic-pump-fabricated-from-scratch/)，它将液体从藏在机器后面的容器中输送到前面的玻璃杯中。该机器有一个 3.5 英寸的 DSI 触摸屏显示器供用户输入，还有一个 WS2812B LED 环，用于在提供饮料时创建一个小型灯光表演。3.3 V 至 5 V 电平转换器用于为 LED 环供电，电机驱动器模块用于驱动蠕动泵电机。它看起来像是有一个“玻璃检测”功能，使用一个 3D 打印的迷你平台，平台上有一个磁铁缺口，这样当一个玻璃放在上面时，霍尔传感器可以检测到附近磁铁的存在。

这个项目的部分魅力在于 Raspberry Pi 上的软件栈，它允许新颖的交互，包括能够从电子邮件的接收中提供饮料。使用 Raspberry Pi 作为控制设备可以提供丰富的接口选项，包括轻松驱动 led、检测玻璃酒杯的存在以及建立网络连接。对于任何想了解这种功能如何转移到他们自己的项目中的人来说，设置过程都记录在存储库中。

饮料搅拌机器人当然是一个东西。从[小可爱](https://hackaday.com/2018/04/09/beautiful-pi-powered-cocktail-machine/)到[满架子](https://hackaday.com/2014/01/21/make-me-a-drink-drinkmo/)不等。