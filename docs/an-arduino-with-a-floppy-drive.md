# 带软驱的 Arduino

> 原文：<https://hackaday.com/2021/04/30/an-arduino-with-a-floppy-drive/>

对于我们许多人来说，软盘的消失是不可记忆的，但是仍然有一群实验者，对他们来说，经典的可移动存储格式仍然有一些魅力。在 8 位微型计算机时代，软驱的接口可能需要一些复杂性，但即使对于今天不太完善的微控制器，这也是一个令人惊讶的简单的硬件前景。[David Hansel]向我们展示了它的风格，一个软驱界面，软件库，甚至是一个简单的 DOS，用于不起眼的 Arduino Uno。

该库提供了允许对软盘进行低级工作的功能，以一个扇区一个扇区地读取它们。此外，它还集成了用于 MS-DOS FAT 文件级访问的 [FatFS](http://elm-chan.org/fsw/ff/00index_e.html) 库，以及允许浏览软盘上文件的 [ArduDOS](https://github.com/dhansel/ArduinoFDC#ardudos) 环境。图片显示了一个 3.5 英寸的驱动器，但它也支持 5.25 英寸的设备以及 DD 和 HD 驱动器。我们可以看到，它对任何使用 retrocomputer 软件试图检索旧磁盘的人来说都是非常有用的，我们期待看到它被纳入一些 retrocomputer 项目中。

当然，Arduino 的用户不需要享受软盘带来的所有乐趣，[树莓派也有一席之地](https://hackaday.com/2021/03/30/a-floppy-controller-for-the-raspberry-pi/)。