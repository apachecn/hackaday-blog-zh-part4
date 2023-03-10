# 三板:缺少键，缺少文档

> 原文：<https://hackaday.com/2022/01/18/threeboard-short-on-keys-long-on-documentation/>

就外设而言，很少有比键盘更受攻击的了。布局、形状、大小、材料，甚至键盘是什么的问题都摆在桌面上等待修补。本着这种精神，[TaylorConor]在 GitHub 上发布了他的简化键盘，名为 threeboard，只有三个键，复制了一个完整的键盘。

我们已经介绍了[带和弦的键盘](https://hackaday.com/2021/08/30/chordie-chording-keyboard-speaks-no-qwerty/)、[环绕咖啡杯的键盘](https://hackaday.com/2021/10/11/cant-spill-coffee-on-your-keyboard-if-its-already-inside/)，以及[带操纵杆的键盘，以提高速度](https://hackaday.com/2021/08/30/chordie-chording-keyboard-speaks-no-qwerty/)。那么为什么要报道这个呢？有什么不同？执行是一流的，是一个很好的例子，看看下次你做一个项目，你想炫耀。键盘只是三个机械开关，两个 8 位二进制显示器(共 16 个 led)，三个状态 led，三个显示当前层(四层)的 led。详细的[用户手册解释了这一切](https://github.com/taylorconor/threeboard/blob/master/documentation/threeboard/threeboard_user_manual.md)。它的核心是一个可靠的 Atmega32U4 微控制器和两个 EEPROM 芯片。

这个项目展示的是测试。它有单元测试、模拟集成测试和模拟属性测试。因为所有的代码都是用 C++编写的，所以单元测试相对简单。集成和性能测试通过模拟器进行。他没有用一些新的标志重新编译代码，而是使用了 [simavr AVR 模拟器](https://github.com/buserror/simavr)，这意味着它模拟了闪存到微控制器上的相同二进制文件。这种方法意味着通过 GDB 对设计进行测试和调试。这是一个令人难以置信的技术，我们希望在业余爱好项目中看到更多。市场营销人士可能会称之为“数字双胞胎”，但这种想法是，你有一个更容易工作的虚拟版本，有一个更紧密的迭代循环，同时尽可能接近物理版本。

[Taylor Conor]的目标是用易读的代码、精彩的文档和最佳实践从头开始创建一个微控制器项目。我们认为他做到了。因此，请随意运行模拟器或直接进入 T2 为自己建造一个模拟器。所有的硬件都在 CERN-OHL-P 的许可下，固件在 GPLv3 的许可下。