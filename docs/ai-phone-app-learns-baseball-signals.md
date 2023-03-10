# AI 手机 App 学习棒球信号

> 原文：<https://hackaday.com/2019/11/24/ai-phone-app-learns-baseball-signals/>

如果你不熟悉一项运动，观看这项运动可能会有点奇怪。例如，大多数美国人会认为板球比赛很有趣，因为他们不知道规则。如果你不熟悉棒球，你可能会奇怪为什么其中一个教练到处挥舞着他的手，摸摸他的鼻子、耳朵和帽子。然而，了解内情的人明白，这是给玩家的一个秘密信号。教练可能会告诉球员偷垒或短打。另一组试图解码信号，但如果你不知道代码，这是众所周知的困难。除非你有下面视频里看到的[机器学习手机 app](https://github.com/Jabrils/Uncle-Rober-Baseball-Predictor) 。

如果你不是棒球迷，它是这样工作的。教练会做很多事情。也许摸摸他的帽子，然后摸摸他的鼻子，刷刷他的左前臂，然后摸摸他的嘴唇。然而，代码往往就像知道一个注意信号和一个动作信号一样简单。例如，教练可能会告诉你，如果他们摸鼻子，然后摸嘴唇，你应该偷。触摸他们的鼻子和耳朵是短打。触摸他们的鼻子和帽舌是另一回事。他们做的任何不是从摸鼻子开始的事情都毫无意义。如果信号这么容易，你真的甚至不需要机器学习来解码它。但如果它更复杂——比如说，在他们触摸鼻子之后出现的第三个手势，除非他们也踢泥土，在这一点上它没有任何意义——人类就更难理解了。

代码使用 [SDEC](https://github.com/Jabrils/SDEC) (序列域包含的相关性)来寻找 ASCII 字符串中的模式。我们不禁会想，这可能也适用于许多其他你在寻找一系列事物的地方。

视频有一个相当不错的关于机器学习的周日增刊解释。它包括一些细节，如隐藏层，而不会陷入太多的数学或实际编码。如果你还没有深入研究机器学习，这不会让你成为专家，但会给你一些指导。

如果你想更详细地解释机器学习是如何工作的，[试试这个](https://hackaday.com/2019/02/22/foundations-for-machine-learning-in-english-or-russian/)。甚至连 [Arduino](https://hackaday.com/2019/06/30/blisteringly-fast-machine-learning-on-an-arduino-uno/) 也能加入进来。

 [https://www.youtube.com/embed/PmlRbfSavbI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PmlRbfSavbI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

