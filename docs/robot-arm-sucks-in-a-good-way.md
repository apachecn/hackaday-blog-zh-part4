# 机器人手臂吸起来很好

> 原文：<https://hackaday.com/2020/04/14/robot-arm-sucks-in-a-good-way/>

制造机器人手臂很有趣，但不再像以前那样具有挑战性。你可以找到很多计划和工具包，驱动电机是一个解决的问题。然而，总有一个决定你必须做出，这可能是一个挑战:什么效应器放在它的末尾。如果你是【MertArduino】答案是[把吸力放在末端](https://github.com/MertArduino/roboticArmVacuum)。如果你需要抓住正确的东西，这可能就是可靠地提起和放下的门票。你可以在下面看到手臂动作的视频。

手臂本身是钢制的，带有四个伺服电机，并附带一个套件。视频显示手臂在手动控制下制作三明治。我们怀疑他可能把它放在 Arduino 的控制之下，但是没有 sudo 来做三明治。

气泵和电磁阀围绕着手臂。一个 Arduino 读取一些 pots 来控制手臂上的伺服电机。然而，空气拾取器是手动控制的。使用 FET 或晶体管将它置于 Arduino 控制之下并不困难。

这让我们想到了过去见过的[气动镊子设计](https://hackaday.com/2017/01/14/daves-not-just-a-member-of-the-air-club-for-tweezers/)。我们还想知道手臂是否足够强壮，可以进行[抓放设置](https://hackaday.com/2019/07/30/pick-and-place-robot-built-with-fischertechnik/)。

 [https://www.youtube.com/embed/eVz7mOJVvQc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eVz7mOJVvQc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

