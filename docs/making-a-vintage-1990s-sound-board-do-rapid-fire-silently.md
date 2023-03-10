# 让一个 90 年代的老式声卡无声地快速发射

> 原文：<https://hackaday.com/2018/08/27/making-a-vintage-1990s-sound-board-do-rapid-fire-silently/>

有时新旧结合比新旧单独使用要好。这就是[布拉德·卡特]在得到一个 90 年代的旧声卡时所了解到的情况，声卡中有一个嘈杂的 SCSI 驱动器。如果你不知道音板是什么，想象一下你面前摆放的一堆按钮，每个按钮播放不同的声音效果。这是电台 DJ 和播客用门铃和汽车碰撞声点缀他们的模式的一种方式。

在获得声卡之前，[Brad]使用了一个现代的触摸屏桌面，但它的响应速度不够快，当快速连续按下一个图标时，声音效果就像机关枪一样重复。另一方面，他的 90 年代声卡有非常灵敏的物理按钮，但 SCSI 硬盘噪音太大。他需要 20 世纪 90 年代物理按钮的响应能力，但需要现代固态存储的安静。

所以[他用一个 SD 卡](http://www.notla.com/archives/2018/08/replacing-my-360-systems-instant-replay-scsi-hard-drive-with-a-memory-card/)替换了声卡的 SCSI 驱动器，SD 卡使用的是 SCSI2SD 适配器。当然，还涉及到配置和格式化，以及一些尝试和错误来获得正确的虚拟驱动器大小。为了避免其他人遇到同样的困难，他在自己的网页上详细描述了自己所有的努力。在下面的视频中，你可以看到和听到最终的结果是惊人的不同。当快速连续按下物理按钮时，会发出即时声音，就像机关枪一样，所有这些都伴随着 SD 卡的静默。

SCSI2SD 卡是一个很好的现成解决方案，但如果你想要一些更定制的东西，那么有一个树莓 Pi SCSI 仿真器和一个使用带有 NCR5380 SCSI 接口芯片的[Teensy。](https://hackaday.com/2016/12/25/the-tiny-scsi-emulator/)

 [https://www.youtube.com/embed/Ser1CEuK02U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ser1CEuK02U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们感谢[radiodork]提供了关于此事的提示。