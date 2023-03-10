# 人工智能机器人扮演恶魔城，所以你不必

> 原文：<https://hackaday.com/2018/12/16/ai-bot-plays-castlevania-so-you-dont-have-to/>

我们不允许在 Hackaday *Wonder Bunker* 这里看电视，但偶尔我们会把他们付给我们的带宽积分凑在一起，围在旧的 3.5 英寸 TFT LCD 周围，看网飞向我们保证 93%喜欢的节目。这就是我们如何发现他们制作了一部基于 NES*恶魔城*比赛之一的电视剧。我们想玩这个游戏来了解背景故事，但由于它来自原始图形必须辅以令人窒息的难度的游戏时代，我们没有走多远。

[![](img/3bd4595e04e06aea372615c2b5d1284b.png)](https://hackaday.com/wp-content/uploads/2018/12/castlevania_detail.png) 但是[多亏了由【迈克尔·伯肯】](https://meatfighter.com/castlevaniabot/)开发的一个非常令人印象深刻的项目，也许在我们攒够足够的学分观看第二季的时候，我们就能搞清楚这一切了(请不要剧透)。他很快指出这个软件是机器学习的例子*而不是*，它试图将他个人关于如何玩*恶魔城*的知识浓缩到 Nintaco NES 模拟器的插件中。最终的结果是 CastlevaniaBot，它能够在没有人工干预的情况下从头到尾播放原始的*恶魔城*。你甚至可以随意停止和启动它，这样它就可以播放完你自己不想做的部分。

[迈克尔]以一个简单的前提开始了这个项目:如果他能让一个机器人成功地通过德古拉城堡的许多关卡，那么让它在途中杀死一些怪物应该是足够容易的。因此，他花了很多时间来完善 CastlevaniaBot 的路径搜索，其中包括手动玩完整个游戏，以便获得背景图像的准确地图。然后对这些图像进行分析，以识别墙壁和楼梯等物体，这样机器人就知道它可以在哪里移动主角西蒙·贝尔蒙特，不可以在哪里移动。无论机器人在游戏中做什么，它总是考虑自己在哪里，需要去哪里，因为每个阶段都有时间限制。

一旦 CastlevaniaBot 知道了它在哪里，要去哪里，以及需要多长时间到达那里，[Michael]就投入了战斗。通过每一帧检查游戏的对象属性内存(NES 视频内存的一部分，用于保存精灵)来识别屏幕上的目标并确定其严重性。在游戏中，打败西蒙所面对的各种生物需要不同的策略，而 CastlevaniaBot 知道所有的策略。机器人将为最优先的敌人部署适当的策略，同时仍然考虑次要目标和最终目标，即在时间用完之前到达阶段的终点。同时模拟器以大约每秒 60 帧的速度运行。

如果这一切听起来让你感兴趣，我们建议你阅读[迈克尔]准备的关于 CastlevaniaBot 的开发及其运作方式的特别详细的文章，因为坦率地说，他比我们更了解它的来龙去脉。当然，如果你宁愿下载 CastlevaniaBot，然后看着它做自己的事情，那也没问题。

这不是我们第一次看到有人黑进一个自动系统为他们玩游戏，但这种利用通常是在最近的游戏和系统上进行的。像为你研磨*塞尔达:野性的呼吸*迷你游戏的 [Teensy 微控制器，或者为 PlayStation Vita](https://hackaday.com/2017/10/25/teensy-script-plays-nintendo-switch-strikes-out/) 躲避*最终幻想 X* 攻击的[按钮敲击伺服系统。](https://hackaday.com/2016/06/22/cheating-at-video-games-arduino-edition/)

 [https://www.youtube.com/embed/UrtgTGmv1GQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UrtgTGmv1GQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

