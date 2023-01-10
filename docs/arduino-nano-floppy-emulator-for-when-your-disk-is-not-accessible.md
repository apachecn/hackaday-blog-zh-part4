# Arduino 纳米软盘模拟器，当您的磁盘不可访问

> 原文：<https://hackaday.com/2021/10/17/arduino-nano-floppy-emulator-for-when-your-disk-is-not-accessible/>

在大量过时的可移动介质中，有一些是令人惋惜的，但很难找到那些对软盘的使用感到遗憾的人。直到 2000 年代初的某个时候，这些硬塑料盖中的柔性磁盘还是计算机的主要产品，它们的驱动器可以在任何备件箱中找到。但是今天，当人们需要一个真正的软驱却找不到的时候，该怎么办呢？进入[Acemi Elektronikci]，带着一个基于 Arduino Nano 的软盘仿真器，它可以插入一台足够旧的 PC 的软盘端口，并允许轻松使用虚拟软盘。

除了 Nano 之外，它还有一个 SD 卡和相关的电平转换器，以及一个 SSD1306 i2c 屏幕。Arduino 的大多数线路驱动软盘接口，因此五按钮控制通过电阻梯到达单个 ADC 引脚。他坦率地承认，它不是原始硬件的完美周期精确仿真器，可能会有机器甚至操作系统在面对它时抱怨，但尽管如此，它是一个有用的工具。可能有问题的机器之一是 Amiga，但幸运的是[有一个树莓派](https://hackaday.com/2013/11/26/raspberry-pi-emulates-an-amiga-500-floppy-drive/)可以解决这个问题。