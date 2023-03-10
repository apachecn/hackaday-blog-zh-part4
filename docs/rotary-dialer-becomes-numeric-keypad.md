# 旋转式拨号器变成数字键盘

> 原文：<https://hackaday.com/2020/07/30/rotary-dialer-becomes-numeric-keypad/>

许多笔记本电脑避免使用数字键盘来腾出空间，一些台式电脑键盘也有这种趋势。如果你想要一个专业的数字输入设备，并且对速度和易用性完全不感兴趣， [[jp3141]正好适合你。](https://github.com/jp3141/rotary_dialer)

这个想法是用旧电话的转盘将数字输入电脑。它缓慢而繁琐，但也相当有趣。该建筑使用一个旧的美国电话电报公司 Trimline 拨号器，虽然我们相信大多数旋转电话将工作。拨号器产生的脉冲由 Teensy 微控制器计数，该微控制器模拟 USB HID 键盘设备，并将相关的按键输入计算机。还有一个用于调试的 USB 串行接口，以及一个随着拨号器电路脉冲闪烁的 LED。

虽然这不是最有效的数据输入方法，但它是重新利用旧手机的一种半有用的方法，也是你下次参加局域网聚会时携带的一件有趣的东西。[我们以前也推出过一些……替代……键盘](https://hackaday.com/2020/05/13/floppy-drive-keyboard-is-inefficient-fun/)。如果你已经为你的电脑设计了一个真正复杂的输入设备，[一定要让我们知道。](http://hackaday.com/submit-a-tip)