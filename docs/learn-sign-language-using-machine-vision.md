# 使用机器视觉学习手语

> 原文：<https://hackaday.com/2022/04/30/learn-sign-language-using-machine-vision/>

学习一门新语言是锻炼大脑和了解不同文化的好方法，有一个母语人士在身边改善学习体验也很好。即使没有，也可以通过视频、书籍和软件来学习。然而，当试图学习一门非口语的语言时，任务确实变得复杂得多，比如美国手语。[这个项目允许用户在计算机视觉和一些机器学习算法的帮助下学习美国手语字母表](https://github.com/albanjoseph/Signapse)。

该构建使用 MobileNetV2 中的计算机视觉模型，该模型针对美国手语字母表中的每个符号进行了训练。在屏幕上向用户显示一个符号，用户需要向计算机演示该符号才能继续。为了做到这一点，OpenCV 运行在带有 PiCamera 的 Raspberry Pi 上，用于实时分析用户的帧。向用户展示正确标志的图片，并在做出正确标志时给予奖励。

虽然目前这仅适用于美国手语中的字母符号，但格拉斯哥大学的团队正在计划将其扩展到其他符号。过去，我们已经看到过其他为教授美国手语而制造的机器，比如这台机器，它依赖于一只专门的手套，而不是计算机视觉。

 [https://www.youtube.com/embed/wkhXxTbKkyo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wkhXxTbKkyo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

