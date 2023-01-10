# 人工智能学会驾驶赛车

> 原文：<https://hackaday.com/2021/01/17/ai-learns-to-drive-trackmania/>

机器学习长期以来一直是人类感兴趣的话题，但只是在最近几年，我们才广泛地获得了强大的计算能力，使普通人能够投入其中。[【Yosh】最近决定让一个人工智能在 *Trackmania 中学习如何比赛。*](https://www.youtube.com/watch?v=a8Bo2DHrrow)

在监督学习的早期实验之后，[Yosh]决定实现一种遗传算法来产生一个在游戏中驾驶的 AI。AI 将距离赛道墙壁的距离作为输入，并将转向和加速器值作为输出。从第 1 代中的 100 个 ai 开始，[Yosh]通过选择在 13 秒内覆盖最长距离的 ai 进行迭代。一旦 AIs 开始掌握前几个弯道的诀窍，他就改变训练，改为优先考虑通过赛道上每个检查站所需的最短时间。

人工智能随着时间的推移而改进，经过 100 多代，在测试跑道上的时间下降到 23.48 秒，而天才人类[特拉巴迪亚]的时间为 19.63 秒。我们很想看看人工智能通过更多的训练能做得多好。[Yosh]正在尝试更多的实验，比如在人工智能健身功能[中提供额外的反馈，以防止它撞到墙上](https://www.youtube.com/watch?v=i1XqbUrarEg&ab_channel=Yosh)。[这也不是我们第一次看到遗传算法被用来训练一个赛车人工智能。](https://hackaday.com/2020/11/07/training-a-neural-network-to-play-a-driving-game/)休息后的视频。

 [https://www.youtube.com/embed/a8Bo2DHrrow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a8Bo2DHrrow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

