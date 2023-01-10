# AI 让 Linux 按你的意思做，而不是按你说的做

> 原文：<https://hackaday.com/2021/04/20/ai-makes-linux-do-what-you-mean-not-what-you-say/>

我们总是羡慕星际迷航企业计算机。你可以问他们一个模糊的问题，他们通常会知道你想要什么。甚至自动门似乎也知道有人走进涡轮电梯和有人在打斗中被扔进门里的区别。[River]决定为一个人工智能服务的私人测试版尝试他的新 API 密匙，以根据描述生成 Linux 命令。它是如何工作的？观看下面的视频，找出答案。

一些例子工作得相当好。作为对“通过电子邮件将 Rickroll 视频发送给杰夫·贝索斯”的回应，系统产生了一个 curl 命令，并向我们认为正确的位置发送了一封电子邮件。“查找当前目录中大于 1 GB 的所有文件”也有效。

当然，像大多数人工智能项目一样，它很容易混淆。“生成三只长颈鹿的图像”创建一个空白图像。出于某种原因，让它下载一些文件似乎也让它感到困惑。让它建议格式化什么硬盘让我们有点害怕。至少它等你来证实它的猜测。

由于许可和成本的原因，你无法完全复制这一点，尽管如果你对深度学习模型足够了解，你可能会接近这一点。然而，我们不能不认为有更好的方法来解决这个问题。

更不用说，shell 命令并没有那么难。我们喜欢正则表达式，但是基于我们要为别人写多少次，也许让它们变得更简单的人工智能会更有趣。同样，[我们有不同的方法](https://hackaday.com/2020/09/11/linux-fu-literate-regular-expressions/)。

 [https://www.youtube.com/embed/j0UnS3jHhAA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j0UnS3jHhAA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

