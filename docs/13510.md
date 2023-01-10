# Aimbot 是用硬件实现的

> 原文：<https://hackaday.com/2022/04/30/aimbot-does-it-in-hardware/>

任何在过去二三十年里玩过在线射击游戏的人几乎肯定都遇到过通过自动瞄准在游戏中作弊的人或机器。对于具有反作弊功能的新游戏来说，这不是一个大问题，但像 Team Fortress 这样的旧游戏实际上已经被这些 aimbots 破坏了。然而，这些类型的作弊通常是在软件中完成的，因此[Kamal]想知道他是否能够[建立一个直接在硬件上工作的 aim 机器人](https://www.youtube.com/watch?v=ne9bmMX82iY)。

首先，我们会提醒每个对 TF2 这样的游戏状态感到沮丧的人，这是一个概念验证机器人，不太可能使任何 aimbots 在任何游戏中变得更糟或更常见。这主要是因为[Kamal]正在训练他的机器在 Aim Lab(第一人称射击训练模拟)中工作，而不是在真正的多人视频游戏中工作。该机器人的工作方式是用 Python 对他的计算机进行截图，并将信息传递给计算机视觉算法，该算法可以识别高对比度目标。从那里，一个 PID 控制器被用来告诉一系列连接到鼠标的全方位轮指向哪里，当光标在点击框中时，鼠标点击被触发。

虽然这看起来很简单，但制造机器人，然后，更重要的是，调整 PID 控制器，花了[Kamal]两个多月的时间，他才能够在 aim 训练器上与职业 FPS 射击运动员竞争。这是一个令人印象深刻的构建，如果他的一个全方位马达没有烧毁，它可能已经超过了平台上最高的人类分数。如果你想要一个让你在游戏中表现更差而不是更好的机器人，那么去[看看这个版本，它通过使用两台电脑在](https://hackaday.com/2021/05/31/teaching-a-machine-to-be-worse-at-a-video-game-than-you-are/)之间传递游戏信息来玩 Valorant。

 [https://www.youtube.com/embed/ne9bmMX82iY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ne9bmMX82iY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

