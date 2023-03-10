# 线性乒乓失去了一个维度，但仍然具有挑战性

> 原文：<https://hackaday.com/2021/01/26/linear-pong-loses-a-dimension-but-remains-challenging/>

当 Pong 在 70 年代初出现时，2D 单色网球游戏的简单性使其足够吸引人，以至于热情的原始游戏玩家通过将他们的硬币盒塞得满满的来短路机器。但是，即使 Pong 的 2D 游戏很简单，问题也变成了:它能不能变得更简单并且仍然可以玩？

令人惊讶的是，如果这个一维乒乓游戏有任何暗示的话，它看起来确实可以。最初的 Pong 让你用球拍对准来球，主要变量是对手的角度，[mircemk]的版本限于线性游戏场地，使球的速度成为变量。玩家通过 WS2812s 的 60 个 LED 条远端的一对按钮来控制游戏。球沿着长条来回移动，只有当球员在球到达的那一刻按下按钮时，球才会从球员的球拍上弹开。每个反射回对手的信号都以随机的速度出现，很难进入节奏。为了增加一些多样性，每个球员都有一个“增强”按钮，为他们的射门增添一点趣味，得分由比赛场地中央的 led 显示。游戏的视频和建造信息在下面。

只需一个 Neopixel 条、一个 Arduino Nano 和少量常见部件，就可以轻松制作出这款令人惊讶的迷人游戏。但是如果 2D 版本仍然更合你的胃口，也许你应该看看它的发明者[Ted Dabney] 的故事。或者，也许建造一个[能和自己一起玩乒乓球的](https://hackaday.com/2018/06/24/clock-plays-a-game-of-pong-with-itself-to-pass-the-time/)来打发时间更合你的胃口。

 [https://www.youtube.com/embed/14-b0aKh2IM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/14-b0aKh2IM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

