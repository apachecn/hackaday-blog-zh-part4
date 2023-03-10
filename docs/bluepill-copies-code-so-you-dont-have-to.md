# Bluepill 复制代码，所以你不必

> 原文：<https://hackaday.com/2020/07/17/bluepill-copies-code-so-you-dont-have-to/>

你真的应该学习阅读莫尔斯电码。但是如果你不能——或者即使你能，只是想休息一下——你总是可以让电脑来做这件事。例如，[jmharvey1]有一个运行在廉价 Bluepill 开发板上的[解码器](https://github.com/jmharvey1/STM32_CWDecoder)。

该设备使用触摸屏和一些常见的组件。整件事大约花了 16 美元。你可以在下面的视频中看到它的工作和项目描述。

代码对蓝色药丸使用 Arduino 风格的设置——这是我们在之前已经讨论过的[。至于解码方法，软件采用 Goertzel 算法，该算法类似于单频傅里叶变换。也就是说，虽然完全变换可以提供较宽范围内信号频率成分的信息，但 Goertzel 算法会探测一个或少量不同频率的信号。](https://hackaday.com/2017/03/30/the-2-32-bit-arduino-with-debugging)

解码器表起初看起来很混乱，直到您意识到每个“解码”值都由 1 作为起始位，后跟 1 的破折号和 0 的点组成。起始位左边的所有位都不计数。因此“E”编码为十六进制的 02——起始位后跟一个零或点。“C”是 1A 十六进制数(1 + -)。-.).一旦找到匹配的代码，就可以将相同的索引应用到另一个表中来查找实际的字母或字母串。

如果你买了一个 Bluepill 来制作其中一个，你也可以买两个来制作一些东西来发送代码。

 [https://www.youtube.com/embed/FaaQbMpAI1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FaaQbMpAI1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

