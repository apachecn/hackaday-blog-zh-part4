# 一个 Arduino 和一个 CD-ROM 驱动器组成一个 CD 播放器

> 原文：<https://hackaday.com/2021/01/03/an-arduino-and-a-cd-rom-drive-makes-a-cd-player/>

在流媒体时代，人们很容易忘记音频 CD，但它们仍然是一种物理格式，从“播放”按钮还不是“支付”按钮的时候就开始了。CD 播放器可能不再像以前那样是珍贵的财产，但如果你喜欢，还是有可能涉足 120 毫米聚碳酸酯光盘的世界。这是[Daniel1111]用他的 [Arduino CD 播放器](https://hackaday.io/project/176545-arduino-cd-player)做的事情，它使用小的微控制器板通过 IDE 总线控制 CD-ROM 驱动器。

该项目大量借鉴了以前实验者的工作，特别是 [ATAPIDUINO](http://singlevalve.web.fc2.com/Atapiduino/atapiduino.htm) ，但它通过从驱动器的 S/PDIF 输出中提取音频来扩展它们。端口扩展器驱动 IDE 接口，而 Cirrus Logic [WM8805 S/PDIF 收发器](https://www.cirrus.com/products/wm8805/)处理数字音频并将其转换为 I ² S 流。进而被馈送到德州仪器 PCM5102 DAC ，该 DAC 提供线路电平音频输出。所有代码和原理图[都可以在 GitHub 库](https://github.com/daniel1111/ArduinoCdPlayer)中找到。

对于任何在 20 世纪 90 年代从事 CD-ROM 业务的人来说，这个项目触动了不少按钮，尽管也许[不足以再次挖出所有那些 CD](https://hackaday.com/2019/03/19/the-cd-is-40-the-cd-is-dead/)。看看 I ² S 流是否可以直接从驱动器内部提升，或者甚至音频数据是否可以通过 ide 总线接收，这将会很有趣。如果你想知道更多关于我的信息，我们为你准备了一篇文章。