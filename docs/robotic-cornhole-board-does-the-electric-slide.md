# 机器人木板做电动滑梯

> 原文：<https://hackaday.com/2020/07/09/robotic-cornhole-board-does-the-electric-slide/>

保龄球道有保险杠，高尔夫游戏有竖杆，这是有原因的。无论你是在学习一项新的游戏或运动，还是已经知道如何玩了很多年但仍然不擅长，每个人都可以在追求胜利的过程中得到一些帮助。你听说过不能错过飞镖板和无砖篮球目标。好了，接下来是机器人辅助游戏:cornhole。

这个游戏本身看起来似乎很简单——只需用手将一个方形的腕托扔进一个稍微倾斜的盒子顶部附近的一个洞里。你甚至可以在箱子上的任何地方落地得一分！如果你在角落里成功了，得三分。实际上，这个游戏并不那么简单，尤其是如果你一直在喝酒(喝酒是被鼓励的)。但是，嘿，这比马蹄铁或草地飞镖安全。

[![](img/c0df143f29fd81c9fc07bab32d96977d.png) ](https://hackaday.com/wp-content/uploads/2020/07/robotic-cornhole-guts.jpg) [【迈克尔·雷希丁】喜欢这个游戏，但并不擅长这个游戏，所以他制作了一个机器人版本，它可以跟踪进来的袋子，并移动洞口来帮助抓住它](https://gizmodo.com/robotic-cornhole-guarantees-victory-assuming-everyone-1844221997)。安装在洞后的网络摄像头拍摄了大量照片，并分析画面的变化。

网络摄像头将其看到的袋子位置及其预测发送到 Arduino，Arduino 决定如何移动一对电机作为响应。在角落里有一对抽屉滑轨，作为盖子的 x/y 门架。

我们喜欢这种方式与其他方式相比的低技术含量，尽管它偶尔会搞砸。没关系——这样会让游戏更有趣。我们认为你应该得到 2 分，如果它降落在洞的一半。休息时间过后，看看构建视频。

似乎现在有一种机器人辅助的运动设备可以做任何事情。如果你不喜欢打高尔夫球，你想不想在高尔夫球赛上打几杆？

 [https://www.youtube.com/embed/FkhxhMJtkHA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FkhxhMJtkHA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[Itay]！