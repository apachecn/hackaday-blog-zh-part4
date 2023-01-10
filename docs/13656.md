# 修理 HDMI 适配器不太顺利

> 原文：<https://hackaday.com/2022/05/16/repairing-an-hdmi-adapter-doesnt-go-so-well/>

[Adrian]有很多 retrocomputers，所以他使用 RGB 转 HDMI 转换器来驱动现代显示器。特别是，他有一个盒子，使用可编程逻辑芯片读取各种 RGB 信号，并将它们发送到一个 Raspberry Pi Zero，以驱动 HDMI 输出。听起来很棒，当然，直到[出了问题](https://www.youtube.com/watch?v=atb04zJ390Q)。

曾经工作的转换器由于带有可编程逻辑芯片的坏板而停止工作。与 retrocomputers 不同的是，这种电路板有很小的表面贴装元件。一点分析表明，一些芯片引脚不接受输入。

Xilinx 器件具有 5V 容差输入，[Adrian]认为 5V 输入可能会烧坏输入，如果引脚上有 5V 电压而器件未上电，就会发生这种情况。计划是移除坏的芯片并用新的替换它。

就 SMD 部件而言，Xilinx 芯片并不是特别小，但如果你更习惯于在 20 世纪 80 年代的电脑上工作，这可能会有点挑战。[阿德里安]明智地使用了大量的焊剂和热空气来删除部分。我们可能会用 Kapton 胶带覆盖相邻的组件，以避免超出我们的期望。

另一个想法是，如果你确定部件是坏的，有时更容易切断所有引线，处理芯片，然后一个接一个地移除每个引脚。不过，他明白了。我们可能会在重新焊接之前清洗焊盘，但[Adrian]选择只添加新的焊料，这确实有效，但多余的焊料使放置新芯片更加困难。

尝试了几次，但坚持是关键。幸运的是，板是高质量的，并采取了大量的热量以及部分。如果你害怕做 SMD 工作，你可能会发现[Adrian 的]旅程很有启发性。他有一台很棒的显微镜，这的确很有帮助。最后，尽管视频捕捉出现了一些问题，造成了一些颜色上的混乱，但它还是工作了。

这并不是一个关于 SMD 返工的教程，更像是一篇第一次写的日记。如果你想要更有指导意义的东西，看看[【Bil Herd 的】帖子](https://hackaday.com/2021/02/02/learn-bil-herds-diy-surface-mount-assembly-process/)。或者，和【摩托极客】共度[一小时。](https://hackaday.com/2017/06/27/an-hour-to-surface-mount/)

 [https://www.youtube.com/embed/atb04zJ390Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/atb04zJ390Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

