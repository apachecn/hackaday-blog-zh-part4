# 树莓派零带轮子的微型战斗机器人

> 原文：<https://hackaday.com/2021/06/12/raspberry-pi-zero-takes-the-wheel-in-miniature-fighting-robot/>

为了利用他对树莓圆周率的熟悉，[[塞巴斯蒂安·赞·塔图姆]决定将小小的圆周率零放在他的“蚁重”战斗机器人的核心， *$hmoney*](https://hackaday.io/project/180238-hmoney-a-combat-robot-powered-by-raspberry-pi) 。虽然听起来早期的道路上有一些颠簸，但这个无尾礼服机器人从最近的休斯顿 Mayhem 2021 比赛中获得了奖项，证明了战斗机器人上的 Linux 年确实已经到来。

与使用传统的业余爱好级 RC 硬件相比，[Sebastian]说使用 Pi 代表了相当大的成本节约。借助 Python 和`evdev`，他能够从商业蓝牙游戏控制器获取输入，并将其转化为 GPIO 连接的电机控制器的命令。特别是对于年轻的竞争对手，这种更熟悉的接口可以被视为优于经典 RC 发射器的优势。

[![](img/4431c75316e36b5916eba2ce97642581.png)](https://hackaday.com/wp-content/uploads/2021/06/pizwbot_detail.jpg) 一个 L298N 板处理两个提供运动的 N20 齿轮电机，而一个塔罗牌 TL300G ESC 负责旋转连接到前面“蝴蝶结”旋转器的无刷电机。添加一个 Turnigy 500mAh 3S 电池组，你就有了一个紧凑而简单的电子封装，可以放入机器人的 3D 打印底盘中。

[在 Reddit 上一个关于 *$hmoney*](https://www.reddit.com/r/raspberry_pi/comments/nt8yg9/presenting_my_first_combat_robot_quite_possibly/) 的帖子中，【Sebastian】回顾了他的团队在与他们一磅重的 Linux 机器人竞争中所学到的一些经验。在俄克拉荷马州的一次活动中，一个过于雄心勃勃的装甲设计让他们付出了巨大的代价，但一个经过调整的底盘最终使他们更具竞争力。

还有一个令人失望的损失，该团队认为这是由于观众中有人试图在战斗最激烈的时候将他们的手机与机器人的 Pi Zero 配对，破坏了控制，让他们死在水中。希望一些改进的软件可以在他们的下一轮比赛之前修补这个漏洞，特别是因为每个阅读 Hackaday 的人现在都知道它了…

虽然这些小规模机器人之间的战斗可能不会像电视比赛那样给 T2 带来同样的激情和愤怒，但它们是让下一代黑客和工程师对建造他们自己的硬件感到兴奋的绝佳方式。我们祝[Sebastian]和*$ hmoney*好运，并期待在未来听到更多他们的战争故事。