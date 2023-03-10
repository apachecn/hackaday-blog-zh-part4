# 自动骰子测试器使用机器视觉来确保公平游戏

> 原文：<https://hackaday.com/2019/06/20/automated-dice-tester-uses-machine-vision-to-ensure-a-fair-game/>

人们非常非常认真地对待他们的桌面游戏。然而，安德鲁·劳里岑在追求公平游戏方面已经做得远远超出了他们的能力。 这款游戏名为*《星球大战:X 翼*，是一款战略战争游戏，游戏中的微型棋子根据骰子的滚动而移动。[Andrew]怀疑商业上可用的骰子扭曲了游戏，休息后视频中显示的自动机器视觉骰子测试器就是结果。

这个装置是一个非常聪明的设计，它以尽可能小的动作最大化数据集。试验箱是一个两端透明的盒子，可以由一个马达端对端翻转；墙壁将室分成四个通道，以测试每次投掷的多个骰子，通道内的挡板确保随机化。一个网络摄像头被放置在试验箱的下方，拍摄每一次“投掷”的快照，然后在 OpenCV 中进行分析。这个方案有一个不幸的效果，就是从桌子的角度看骰子，但[Andrew]以真正的黑客方式处理了这个问题:他忽略了它，因为它不会影响他感兴趣的统计数据。

说到统计，他创造了很多统计数据。[62 页的研究结果报告](https://docs.google.com/document/d/1alv05cXh0WhNaFPoq3LNzxmv6veurf6utV1kMQAYDQw/edit#heading=h.bojve7q9v4yt)是一份令人印象深刻的工作，它基本上得出结论，由于制造的可变性，骰子是不公平的，玩家可以利用这一事实作弊。他建议在竞争游戏中用一组骰子来消除优势。

这不是我们在这些地方看到的第一个自动掷骰子的人。有发微博的掷骰子机器人、自动掷骰子机器人和各种各样的电子掷骰子机。这一次为保持公平付出了额外的努力，我们对此表示感谢。

 [https://www.youtube.com/embed/YTFamRKdVT8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YTFamRKdVT8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[gadwag]告诉我们这个。谢谢！