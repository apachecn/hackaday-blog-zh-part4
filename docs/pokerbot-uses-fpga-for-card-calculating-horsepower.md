# 扑克使用 FPGA 卡计算马力

> 原文：<https://hackaday.com/2019/05/16/pokerbot-uses-fpga-for-card-calculating-horsepower/>

与人类对战，扑克是一种既能读懂对手，又能读懂你手中牌的游戏。这并不意味着没有特定的数学方法来帮助你基于概率做出决策。在这种情况下，康奈尔大学 ECE 5760 班的一群学生在 FPGA 上制作了一个 pokerbot。

该机器人使用蒙特卡洛模拟原理来计算个人赢得德州扑克一手牌的概率。计算整组可能的手牌是不切实际的，所以在蒙特卡罗模拟中，计算的是一个样本。通过在 FPGA 上加速这些计算，pokerbot 能够在 150 毫秒内计算出 300，000 手可能的牌，并向人类玩家展示获胜的概率。同样的计算方法也用于游戏中电脑玩家的决策。

该团队报告称，与在英特尔 i7-6700HQ 上运行的 C++程序相比，FPGA 的处理能力提高了 10 倍。强大的统计计算有助于使电脑玩家参与和现实的比赛。

这是 Bruce Land 的课程中的另一个很好的例子，[这些课程是每年发展的温床](https://hackaday.com/2017/01/11/this-bike-sonar-is-off-the-chain/)。休息后的视频。

 [https://www.youtube.com/embed/utOuXsdpRrQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/utOuXsdpRrQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

