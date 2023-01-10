# 手持法克尔真的闪闪发光

> 原文：<https://hackaday.com/2021/01/18/handheld-farkle-really-sparkles/>

Farkle 是一个经典的骰子游戏，只需要 6 个骰子和一种根据掷出的数字写下分数的方法。即便如此，这种游戏本质上并不便于携带——例如，在公路旅行中玩起来相当困难。他认为法尔科将会制作出一款出色的电子游戏，并开始设计他的第一个印刷电路板。

这个小游戏有你想要的一切，从一个闪屏介绍到一个方便的得分指南。选择玩家人数后，第一个玩家使用瞬时按钮掷骰子，电子骰子亮起以指示掷出了什么。只要玩家掷出至少一个得分骰子，他们就可以通过用 capsense pads 选择适当的骰子来得分，要么通过，要么继续。当前玩家的分数显示在 7 段上，每个玩家的总分数显示在底部的有机发光二极管屏幕上。

操作的大脑是 Arduino Pro Mini。它控制两个 MAX7219s，驱动 42 个 led 和 7 段显示器。像这样的游戏都在代码中，幸运的是，[Sunyecz22]使它可用。我们喜欢光滑的 3D 打印外壳看起来多么华丽-在光滑的表面和弯曲的背部之间，它看起来非常舒适。未来，[Sunyecz22]计划制作一个单人对战电脑模式的游戏。休息之后，请观看演示和演练视频。

capsense 模块是一个很棒的触摸，但有些人希望他们的手持游戏有更多的触感。我们说打开拨动开关。

 [https://www.youtube.com/embed/ZD5JAOXKMG4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZD5JAOXKMG4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

