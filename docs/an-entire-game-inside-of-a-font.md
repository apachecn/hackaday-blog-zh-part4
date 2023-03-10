# 字体中的整个游戏

> 原文：<https://hackaday.com/2021/03/22/an-entire-game-inside-of-a-font/>

你最不希望在电脑上玩游戏的地方是哪里？文字处理程序？图像编辑器？你的文本编辑器怎么样？没错——你可以在任何使用字体的程序中与你的 Fontemons 战斗，因为 mad genius [Michael Mulet]已经创建了一个完全存在于单个开放类型字体文件中的游戏。

[迈克尔]已经利用连字的力量创造了一个选择你自己的冒险风格的回合制游戏，它嘲笑口袋妖怪和各种字体名称。你首先要在纸莎草狂、维尔丹塔和普罗吉托之间做出选择，然后面对像赫尔维蒂汗和斯科里尔这样的敌人。

[![](img/cb07a12524a4d7210006a8214ef58ebe.png) ](https://hackaday.com/wp-content/uploads/2021/03/fontemon-gimp.png) [这是因为在屏幕上画字形有很多种方法](https://github.com/mmulet/code-relay/blob/main/markdown/HowIDidIt.md)。[Michael]选择了 Type 2 Charstrings，这是 Adobe 为 PostScript 创建的一种矢量图形格式。它可以使用一系列移动规范来绘制像素，这些规范告诉它向上、向右绘制，然后在使用从起点绘制到终点的隐式运算符关闭像素之前返回。[迈克尔]能够通过绘制较小版本的像素来创建两种灰度，并通过组合白色和黑色像素来制作图像。

如果你只是想玩游戏，你可以下载。otf 文件或者只是在浏览器中试用一下。你应该使用“a”和“b”来选择推进游戏，但我们很快发现，像“v”和“Enter”这样的垃圾键会导致奇怪的地方。如果你直接玩它，大约需要 20 分钟，但有足够的内置秘密使它持续五倍长。[迈克尔]很友好地为[创建了一个制作基于字体的游戏的教程](https://github.com/mmulet/code-relay/blob/main/markdown/Tutorial.md)，但是如果你只是想开始玩，[游戏引擎是开源的](https://github.com/mmulet/font-game-engine)。

在锁定的工作电脑上，你还能做些什么有趣的事情呢？如果它有 Excel，[你可以用它来制作动画](https://hackaday.com/2019/08/29/experiments-in-3d-graphics-via-excel/)或者只是[放松一下，看看电影](https://hackaday.com/2014/10/24/using-excel-to-watch-movies-at-work/)。