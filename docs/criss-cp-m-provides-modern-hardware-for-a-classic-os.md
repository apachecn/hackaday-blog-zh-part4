# CRISS CP/M 为经典操作系统提供了现代硬件

> 原文：<https://hackaday.com/2021/08/30/criss-cp-m-provides-modern-hardware-for-a-classic-os/>

今天，你可能会选择在你的电脑上运行 Windows、Linux、MacOS 或其他操作系统。然而，回到 20 世纪 80 年代，你通常没有什么选择:某台家用电脑配有某个操作系统，仅此而已。如果您的系统基于 Z80 处理器，那么它很有可能运行 CP/M。虽然硬件上的差异常常使直接数据交换变得困难，但 CP/M 至少在各种基于 Z80 的计算机之间提供了基本的软件兼容性。尽管最终被 MS-DOS(最初的目标是与 CP/M 兼容)取代，爱好者们在整个 90 年代甚至更久的时间里一直让这个经典的操作系统在旧的硬件上运行。

[Igor]决定通过设计主要基于 AVR 微控制器的单板计算机 [CRISS](https://hackaday.io/project/181038-criss-cpm-8-bit-homebrew-diy-computer-avr-based) 来制造 21 世纪的 CP/M 机器。CPU 是 20 MHz 的 ATMEGA1284P，它通过机器码仿真来模仿 4 MHz 的 Z80。一对 ATMEGA328s 运行外围控制器和 VGA 输出，因此 CRISS 可以与现代监视器一起使用。然而，与其传统一样，该图像是黑底绿色的单色图像，对于 Kaypros、Osbornes 和其他当代 CP/M 机器的用户来说，看起来非常熟悉。

软件通过存有软盘映像的 SD 卡加载。CRISS 可以直接运行为 Kaypro II 和 Robotron 1715 计算机编写的程序，尽管通过软件升级也可以支持其他平台。[Igor]展示了它运行的程序，从 Turbo Pascal 编译器到 Xonix 和俄罗斯方块等游戏。

CRISS 装在一个整洁的小盒子里，可以与标准 PS/2 键盘和串行打印机通信。甚至为那些愿意尝试网络连接的人提供了一个以太网端口(这在 20 世纪 80 年代是一个罕见的功能)。

我们喜欢看到这样的现代复古建筑；我们之前报道过的类似项目包括紧凑型 [ZZ80MB](https://hackaday.com/2020/10/28/this-z80-computer-bootstraps-itself/) 和大型 [Z20X](https://hackaday.com/2020/02/23/a-z80-computer-at-the-next-level/) 。其他人在现代硬件上使用不同的方式运行 CP/M，比如在树莓 Pi 上直接启动[或者在 ESP32](https://hackaday.com/2016/10/12/raspberry-pi-boots-cpm/) 上模拟 Altair [。](https://hackaday.com/2020/08/20/esp32-altair-emulator-gets-split-personality/)