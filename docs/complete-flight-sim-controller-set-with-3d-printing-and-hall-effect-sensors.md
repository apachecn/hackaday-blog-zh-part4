# 配有 3D 打印和霍尔效应传感器的完整飞行 Sim 控制器套件。

> 原文：<https://hackaday.com/2020/10/26/complete-flight-sim-controller-set-with-3d-printing-and-hall-effect-sensors/>

[Tom Stanton]最近一直在玩微软飞行模拟器，并决定他的旧桌面操纵杆需要升级。他没有仅仅用一个更新的商业模型来取代它，而是建造了一个完整的控制器系统，它有一个可以在地板上枢转的长操纵杆、集成的方向舵踏板和一个油门盒。休息之后你可以看到它的实际效果。

操纵杆的行程受到[Tom]的腿和椅子的限制，在任一轴上只有 12°的行程，这对于电位计的高分辨率来说太小了。相反，他使用霍尔效应传感器和每个轴的方形磁铁，这在小投掷角上提供了良好的分辨率。连接两个方向舵脚蹬的枢轴也利用了霍尔效应传感器，但需要更多的行程。为了增加磁场的大小，[Tom]在传感器的两侧安装了两块磁铁，它们的磁极对齐。为了使方向舵脚蹬和操纵杆居中，增加了几个长拉伸弹簧。

![](img/255b786b063cb9a85c24eae58781c329.png)

The joystick (left) and rudder pedals (right) magnet configurations with a hall effect sensor.

油门杆上使用了一个普通的电位计，[Tom]还增加了一些额外的拨动开关和按钮，用于定制功能。该系统的框架由 T 形槽挤压件制成，因此组件可以快速移动以适应特定用户，并调整对中弹簧的预载。所有的电子元件都连接到一个 Arduino Micro，由于有了一个[操纵杆库](https://www.youtube.com/redirect?v=XcKmBWGFUn8&redir_token=QUFFLUhqbGhtSExmMHl1cW0xLWhXb1BZY1I0WG9mM3FlQXxBQ3Jtc0tsbW1hOGNyT1ctXzdySkxVaFlBdUVpbEk2UmxFb3JjVnZSOXlRdGY2ak92VzdOMHVyWFU3bzVtMDV5OGdELVRmcmNyUk10Q01zVFAzNmhoMmZGTXJvQ0RobTRNMWlMMkpPQ3J4dE93OW84SFVrR2FEaw%3D%3D&event=video_description&q=https%3A%2F%2Fgithub.com%2FMHeironimus%2FArduinoJoystickLibrary)，代码非常简单。

总建造成本为 212/275 美元，这当然不算便宜，但也低于你为商业产品支付的费用。如果你想自己制作，所有的设计文件和制作细节都在第二个视频中链接。

随着最新的 MS 飞行模拟器的发布，飞行模拟控制器的版本将会越来越多。有了 3D 打印，你可以用操纵杆和油门来增强 Xbox 控制器，或者仅仅使用胶带和一些电子元件，就可以把书桌抽屉变成飞行轭。

 [https://www.youtube.com/embed/SgqflcHBTwc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SgqflcHBTwc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/XcKmBWGFUn8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XcKmBWGFUn8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

