# 老式飞机控制转 USB 按钮盒

> 原文：<https://hackaday.com/2020/07/25/vintage-aircraft-controls-turned-usb-button-box/>

Gables Engineering G-2789 音频选择器面板在安装它们的飞机外部并不太好，直到[【melkorscreatesthis】用一个 Teensy 3.2](https://imgur.com/a/W4oCyuZ) 取代了大部分内部部件。现在，它们是多功能 USB 输入设备，适用于…嗯，无论你用一堆挂在电脑上的拨动开关和瞬时按钮做什么。

[![](img/3e0a66cab140831be1807d800b934750.png)](https://hackaday.com/wp-content/uploads/2020/07/gablesbuttons_detail.jpg)

Tracing wires from the panel switches.

随着 Teensy 成为 USB 游戏控制器的最佳印象，主机操作系统可以访问七个瞬时按钮，十二个开关和一个音量旋钮旋转轴。

现在[melkorscreatesthis]说代码已经设置好了，所以计算机在每次状态改变时都会看到一个按钮被按下；换句话说，分配给拨动开关的按钮将在抬起时被“按下”一次，在弹回时又被“按下”一次。当然，这可以根据你想与设备连接的软件类型进行修改。

[正如我们在其他老式飞机仪器上看到的一样](https://hackaday.com/2018/07/24/milspec-teardown-c-1282-chaff-controller/)，G-2789 上的照明由一系列白炽灯泡提供，它们透过不透明的前面板材料发光。[melkorscreatesthis]用白色 led 取代了那些灯，但不幸的是，产生的光有点太刺眼了。作为一个快速解决方案，led 被涂上了几层黄色和橙色的油漆，直到灯光变成琥珀色。使用 RGB LEDs 本来是一个不错的选择，但你只能利用现有的东西。

这不是第一次[【melkorscreatesthis】将一个旧的飞机驾驶舱模块变成 USB 输入设备](https://hackaday.com/2019/06/13/up-your-game-with-a-battle-tested-input-device/)，我们当然有兴趣看看下一个项目会是什么样子。虽然我们可能更感兴趣的是找出所有这些旧的学校飞机零件是从哪里来的…