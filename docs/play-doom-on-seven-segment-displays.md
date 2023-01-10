# 在七段显示器上玩毁灭战士

> 原文：<https://hackaday.com/2022/10/29/play-doom-on-seven-segment-displays/>

让 *DOOM* 在一台本不该运行的电脑上运行，在深奥的复古电脑世界里是一个有趣的比喻。到目前为止，我们已经看到它运行在从旧 NES 系统到微波炉，跑步机，以及基本上任何内置电脑的东西上。我们不常看到的是显示器本身是专门为运行经典射手而设置的。这个版本可能会在普通硬件上运行游戏本身，但令人印象深刻的是，它能够在这个七段显示器上显示[。](https://www.reddit.com/r/itrunsdoom/comments/yedyg9/doom_on_a_sign_made_out_of_sevensegment_digits/)

这种构建广泛使用多路复用器来驱动足够多的七段显示器，以用作可通行的屏幕。有 1152 个七段数字排列成 48×24 阵列，由菊花链 MAX7219 芯片网络供电。在 Raspberry Pi 上运行的 Python 脚本将实际图像数据与要在每个片段上显示的数字相关联，Raspberry Pi 将所有这些信息发送到屏幕上。最终的结果是显示器足够快，足够准确，以一种真正独特的方式播放 *DOOM* 。

在他们的[项目页面](https://sss.readthedocs.io/en/latest/)上有更多关于这个项目的可用信息，并且他们已经为那些希望跟进的人开放了所有的资源。这个项目不仅仅包括玩*末日*的能力。有一个内置的视频播放器和一些专门利用这种显示器的街机程序。也许有一天，我们也会看到类似的东西移植到[的十六段显示器](https://hackaday.com/2022/10/08/ill-see-your-seven-segment-mechanical-display-and-raise-you-to-16-segments/)上，而不是更常见的七段显示器。