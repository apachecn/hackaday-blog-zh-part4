# Picovoice 在 512K 内存中使 Smarts 离线

> 原文：<https://hackaday.com/2019/01/01/picovoice-puts-smarts-offline-in-512k-of-memory/>

我们生活在未来。你可以让你的私人助理打开灯，计划你的通勤，或者设置你的恒温器。如果他们给 Alexa sudo，她也许能做个三明治。然而，你几乎总是看到这些设备将数据发送到空中的某个远程服务器进行分析和处理。这有一些好处，但正如最近的几则新闻报道所指出的那样，这对隐私没有好处。当网络或远程服务器崩溃时，它也不能很好地工作——这是另一个最近的新闻故事。但是有什么选择呢？如果 [Picovoice](https://picovoice.ai) 成功了，你就可以离线进行所有的语音识别了。

看看下面的视频。有一个臂板，和我们在 Hackaday 掩体中放的几个臂板没有太大区别。它正在监听唤醒短语并处理音频命令。全部在大约 512K 的内存中。[库](https://github.com/Picovoice)显然非常便携，Linux 和 Raspberry Pi 版本已经是开源的。该公司表示，他们将在即将发布的版本中提供其他平台，并声称支持 ARM Cortex-M、Cortex-A、Android、Mac、Windows 和 WebAssembly。

我们认为这是真的，因为你可以在视频中看到 ARM 版本的工作，并且在他们的网站上有基于浏览器的演示。他们说代码是用 ANSI C 编写的，使用定点数学来完成所有的神经网络魔术，所以代码应该是可移植的。

GitHub 上的库包括:

*   rhino–语音到意图(换句话说，做一些事情来响应口头命令)
*   豪猪–唤醒词检测
*   cheetah–语音转文本

事实上，这是一个令人兴奋的开源技术，我们很有兴趣看看你会用这项技术做什么。如果你建造了一个语音控制的啤酒酿造设备——或其他任何东西——一定要通过[提示热线](https://hackaday.com/submit-a-tip/)让我们知道，这样我们就可以与每个人分享它。

 [https://www.youtube.com/embed/WadKhfLyqTQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WadKhfLyqTQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

