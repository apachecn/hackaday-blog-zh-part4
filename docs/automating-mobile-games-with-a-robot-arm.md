# 用机械臂自动化手机游戏

> 原文：<https://hackaday.com/2021/11/28/automating-mobile-games-with-a-robot-arm/>

《我的歌唱怪兽》是一款让用户通过玩简单的游戏来赚取硬币和宝石的手机游戏。[Anykey]发现他的儿子是这个游戏的粉丝，但有时感觉有点作弊。因此，他没有浪费时间玩游戏，而是让一个机器人替他们做这项工作。(超无聊视频，嵌在下面。)

玩家必须完成一个基本但耗时的记忆游戏。获胜后，玩家可以从 17 张神秘卡片中选择一份奖品。1000 颗钻石的头奖似乎总是藏在另一张牌下面，导致了前面提到的挫败感。

为了测试游戏是否被操纵，[Anykey]设置了一个 uArm Swift Pro 来玩游戏，机械臂在 iPad 上移动一个小手写笔来玩游戏。iPad 的视频通过 HDMI out 传输到 PC，进入 Camlink 采集卡。然后创建了一个使用 OpenCV 的 Python 脚本来自动玩游戏，并记录沿途获得的奖励结果。所有的代码都在 GitHub 上。

在尝试了 100 多次之后，机器人始终没有找到正确的牌来赢得 1000 颗钻石。鉴于只有 17 张牌可供选择，人们会认为 1000 钻石奖会在这么多选择中出现几次。

看来，完成记忆游戏的奖品选择实际上并不在于选择正确的卡片。取而代之的是，所给的奖励完全是通过一些其他的计算来选择的。

我们喜欢在 Hackaday 玩游戏的机器人，即使它像井字游戏一样简单。休息后的视频。

 [https://www.youtube.com/embed/kqX2fnt7vmg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kqX2fnt7vmg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

