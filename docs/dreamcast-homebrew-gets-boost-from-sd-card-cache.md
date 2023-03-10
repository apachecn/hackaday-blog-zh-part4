# Dreamcast 自制软件从 SD 卡缓存中获得提升

> 原文：<https://hackaday.com/2021/06/04/dreamcast-homebrew-gets-boost-from-sd-card-cache/>

虽然与当代游戏机相比，它可能是一个商业上的失败，但世嘉 Dreamcast 在发布二十多年后仍然享有活跃的家酿现场。部分原因是因为你可以在标准 CD-r 上刻录可播放的 Dreamcast 光盘，但该系统的粉丝也会指出，该机器在许多方面显然领先于时代，这在社区中给了它一点额外的善意。

同一个社区现在也在讨论著名的 Dreamcast 黑客[【Ian Micheal】如何通过控制台的串口](https://www.dreamcast-talk.com/forum/viewtopic.php?f=2&t=14496)将数据缓存到 SD 卡的消息。在大约 600 KB/s 的速度下，该界面太慢了，无法将其用作交换空间来扩展系统微不足道的 16 MB 内存，但它足以加载游戏资产，否则这些资产将必须加载到 RAM 中。

[![](img/dc80536356023a39d82e2e703be8b118.png)](https://hackaday.com/wp-content/uploads/2021/05/dcsdcache_detail.jpg)

A third-party [Dreamcast SD adapter](https://www.youtube.com/watch?v=sAX-_Vzq6mg).

在下面的视频中，[Ian]展示了他的新技术，在 640×480 下运行一个毁灭之港。他已经看到了帧速率的提高，并认为进一步的优化应该允许稳定的 30 FPS，但这并不是最令人兴奋的部分。当游戏运行时，从 SD 卡中加载基本上无限量的数据的能力，这打开了运行 mods 的可能性，否则这是不可能的。它还应该允许像保存截图或游戏进度到 SD 卡的细节，以便于检索。

[Ian]表示，他将在不久的将来将相同的技术引入他的 Dreamcast ports of Quake 和己烯，并计划在 GitHub 上发布一些演示读写 FAT32 卡的代码，以便其他开发人员也能分享这一乐趣。缺点是，你显然需要有一个 SD 卡适配器插入到你的控制台来利用这项技术，这不是每个人都会有的。幸运的是，它们现在相当便宜，但如果价格开始攀升，我们也不会感到惊讶。如果你还没有，现在可能是时候买一个了。

需要明确的是，这项技术与用 SD 卡替换 Dreamcast 的光驱完全不同，sd 卡替换光驱是一项非常受欢迎的修改，它帮助世嘉的最后一台家用游戏机持续运行时间远远超过任何人的想象。

 [https://www.youtube.com/embed/ERqCmSLm_ok?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ERqCmSLm_ok?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢小卡的提示。]