# 树莓派的软驱控制器

> 原文：<https://hackaday.com/2021/03/30/a-floppy-controller-for-the-raspberry-pi/>

树莓派是每个人的最爱单板电脑。Pi 400 模仿了 20 世纪 80 年代非常流行的一体式键盘电脑设计，甚至点亮了老一代电脑的眼睛。另一个可以追溯到那个黄金时代的项目是 Scott M. Baker 博士]的 Raspberry Pi 软盘控制器板。

[Scott]对软盘控制器并不陌生，他曾在 RC2014 家酿 Z80 计算机上使用过流行的 WD37C65 软盘控制器 IC。因此，当他希望在 Raspberry Pi 上实现一个软盘接口时，这是他的一部分选择。这项工作很简单，只需要 IC 本身就可以完成。尽管 Pi 在 3.3 V 下运行，控制器在 5 V 下运行，但[Scott]到目前为止没有发现任何问题，只是实施了一个电阻包，试图限制控制器将更高电压信号发送回 Pi 造成的损害。也就是说，他计划实现一个合适的电平转换器，以确保长期无故障运行。

这个项目是用一堆 Python 工具来完成的，这些工具用来与控制器接口，可以在 Github 上找到[。性能受到 Raspberry Pi 用户模式操作的非实时性的限制，[Scott]指出这可以通过内核模块来解决。也就是说，如果你正在寻找性能，无论如何软盘不是它。](https://github.com/sbelectronics/pi-fdc)

我们确实喜欢在复古任务中使用 Pi；如果你需要一把，它甚至可以是一把 SCSI 瑞士军刀。休息后的视频。

 [https://www.youtube.com/embed/I6E7oM7EDcc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I6E7oM7EDcc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Baldpower 的提示！]