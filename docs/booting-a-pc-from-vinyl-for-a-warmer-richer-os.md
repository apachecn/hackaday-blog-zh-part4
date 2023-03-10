# 从黑胶启动电脑，运行更温暖、更丰富的操作系统

> 原文：<https://hackaday.com/2020/11/23/booting-a-pc-from-vinyl-for-a-warmer-richer-os/>

如果你浏览过任何一台 PC 的 BIOS 提供的引导选项列表，它读起来就像是存储技术的历史。在顶部，我们有从磁盘启动的选项，通常是固态驱动器，然后是 USB 磁盘、光驱、可移动介质，在底部，通常有从网络启动的选项。然而，实际上没有 BIOS 可以选择从黑胶唱片引导电脑，至少到目前为止是这样。

很明显这个项目来自于“为什么不呢？”黑客学院的 Jozef Bogin 提出了 IBM-PC 的正常启动过程。如*IBM-PC——5150 型，油灰色外壳，双 5-1/4”软盘，以及一个令人惊叹的带有绿色慢衰减荧光粉的单色显示器。为了达到这个目的，[Jozef]利用了早期个人电脑很少使用且鲜为人知的盒式磁带接口。这需要建立一个新的引导加载程序，并将其烧录到 ROM 中，以使 PC 通过其 8255 可编程外设接口芯片来收听音频信号。*

 *一旦电脑有了正确的引导程序，一个 64k 的 FreeDOS 可引导磁盘映像就被记录在黑胶上。[Jozef]除了提到音频被直接发送到乙烯基车床之外，几乎没有提供关于该过程的细节；我们很想了解更多。尽管如此，最终的 10”记录，以 45 RPM 的速度播放，并进行一些均衡调整以适应前置放大器的 RIAA 均衡曲线，可以很好地将 PC 引导到 FreeDOS，可能不会比从软盘引导花费更多的时间。

这可能不是我们第一次在黑胶上看到[软件，但它仍然是一个非常酷的黑客。想自己试试却缺少一台破纪录车床？也许](https://hackaday.com/2019/11/24/secret-c64-program-found-on-a-christian-rock-bands-vinyl-record/)[激光切割你的引导盘](https://hackaday.com/2015/08/07/laser-cut-your-own-vinyl-records/)会奏效。

 [https://www.youtube.com/embed/bqz65_YfcJg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bqz65_YfcJg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[约翰]和其他一些人在这件事上给我们提供了线索。*