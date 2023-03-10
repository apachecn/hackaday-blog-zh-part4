# Arduino 腕表配有 LED 指针

> 原文：<https://hackaday.com/2020/01/05/arduino-wristwatch-has-led-hands/>

当你阅读“Arduino 腕表”时，你会陷入想象 Arduino UNO 笨拙地绑在某人手腕上的陷阱。【Marijo bla EVI】[的创作比](https://www.hackster.io/marijoblaz/arduino-wristwatch-d4cc92)的要精致得多。圆形电路板容纳两个表面贴装集成电路和 12 个发光二极管。整个东西看起来很好，紧贴在表体内。它不是劳力士，但它确实有相当高的极客信誉，在上流社会也不会过时。

当然，其中一个 IC 是 AVR micro。另一个是内置晶振的 DS3231 实时时钟。一台 CR2032 让它一直运转。主体、外环、底部和按钮都是用 PLA 3D 打印的。水晶和表带是唯一没有印刷的机械零件。[物料清单](https://docs.google.com/spreadsheets/d/1dRS8NlPdyWTDZ6p1nXBYItXKkWj21toqLvILf9NTu7Y/edit#gid=0)展示了一个 36 毫米的水晶，甚至提供了所有零件的链接。

你不想一直开着 led 灯，因为它对电池不好。当你按下按钮一次，你会得到一个发光二极管来显示小时。另一台印刷机以 5 分钟为单位读取分钟。第三次按下会显示五个 led 中的一个，以显示要添加多少分钟。例如，如果时间是 9:26，您将得到 LED 9(小时)，LED 5 显示 25 分钟，第三次按下将显示 LED 1 多一分钟。如果任何一个分钟指示器显示 12 点，则表示零分钟。

当然，令人兴奋的是，你可以在 GitHub 上编写超过[代码](https://github.com/marijoblaz/iOWatch)的程序。它已经可以显示时间和温度。你没有太多的 I/O，但是如果你尝试的话，你应该可以得到更多的选择，也许还可以得到一些闪光的 LED 闪烁模式。