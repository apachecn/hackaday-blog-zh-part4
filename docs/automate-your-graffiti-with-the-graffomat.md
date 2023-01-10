# 使用 Graffomat 自动涂鸦！

> 原文：<https://hackaday.com/2021/09/30/automate-your-graffiti-with-the-graffomat/>

在班克斯的书*墙与片*里，有一段很有意思的引用；“想象一个涂鸦不违法的城市，一个每个人都可以画自己喜欢的任何东西的城市…”。这听起来像是一个非常令人兴奋的城市，除了我们这些没有艺术细胞的人。幸运的是，[尼克拉斯·罗伊]已经想出了解决这个问题的办法；[Graffomat，一个喷罐绘图仪](https://github.com/royrobotiks/Graffomat)。

用创作者自己的话来说，Graffomat 是一个“快速而肮脏的涂鸦绘图仪”。它主要由木材制成，由回收的无绳钻机驱动，拉动绳轮来移动门架。Graffomat 的核心 Arduino Nano 可以通过串行发送坐标来控制。这允许连接一个 SD 读卡器来滴喂机器，或连接一台计算机来实现实时本地或互联网控制。

我们对[Niklas]处理位置跟踪的方式印象特别深刻。无绳电钻肯定不像步进电机那样可重复，以允许开环控制。因此，需要主动跟踪机架和头部的位置。为了实现这一点，轴上覆盖了黑白条纹编码条，然后在机器移动时由一对光电晶体管读取。然后，这些可以与左上角的归位开关配对，以确定绝对位置。

Graffomat 并不是我们报道的第一台自动涂鸦机器。在这里阅读关于在爱沙尼亚爬烟囱画壁画的机器人。

 [https://www.youtube.com/embed/Pz5CftU_bJw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Pz5CftU_bJw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [r/arduino](https://www.reddit.com/r/arduino/comments/pxt1xk/two_old_cordless_drills_as_muscle_and_an_arduino/)