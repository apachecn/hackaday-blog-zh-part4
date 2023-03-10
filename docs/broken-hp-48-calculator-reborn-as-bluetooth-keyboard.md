# 残破的 HP-48 计算器重生成蓝牙键盘

> 原文：<https://hackaday.com/2019/08/16/broken-hp-48-calculator-reborn-as-bluetooth-keyboard/>

考虑到它们的硬件规格，图形计算器在 2019 年肯定感觉是一个时代错误。现在有大量的应用程序和其他软件可以用来计算，尽管我们的老师都在说教，但我们实际上每天都带着计算器。另一方面，当使用物理旋钮和按钮而不是触摸屏或鼠标输入时，永远不要低估肌肉记忆的力量。[epostkastl]结合了这两个世界的优点，[将他坏掉的 HP-48 变成了一个蓝牙 LE 键盘](https://www.instructables.com/id/Bluetooth48G-Upcycle-Broken-Hp48G-Keyboard/),以获得其模拟对手的真实感受。

最初实现为 [USB 设备](https://www.instructables.com/id/USB48G-Upcycle-Broken-Hp48-Keyboard/)，【epostkastl】这次选择了无线版本，并将基于 nRF52 的 Adafruit 羽毛板连接到 HP-48 方便暴露的按钮矩阵引脚。对于软件仿真方面，他使用 Emu48，这是一个用于 Windows 和 Android 的开源惠普计算器仿真器。Emu84 的伟大之处在于，它支持完全可定制的常规键盘事件到模拟按钮的映射，因此您可以轻松地将余弦按钮映射到`[C]`键。剩下的就很简单了:扫描按钮矩阵检测按钮按压，将它们映射到一个按键事件，并将其作为 BLE HID 事件发送到运行 Emu84 的接收端。

因为这将[epostkastl]的 HP-48 本质上变成了一个紧凑封装的普通无线键盘——尽管其布局超越了每一场*QWERTY vs Dvorak*辩论。当然，它也可以找到替代的使用案例，例如媒体中心遥控器或快捷键。毕竟，我们之前已经见过后一个被建成为[踏脚转盘](https://hackaday.com/2018/01/19/a-keyboard-to-stomp-on/)和[手指训练设备](https://hackaday.com/2018/09/20/this-keyboard-and-mouse-also-gives-you-a-workout/)的，那么为什么不是计算器呢？

 [https://www.youtube.com/embed/EPaNfpmFbIg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EPaNfpmFbIg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

