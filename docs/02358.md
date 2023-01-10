# 智能 Raspberry Pi 摄像头—云还是本地？

> 原文：<https://hackaday.com/2019/03/07/raspberry-pi-camera-with-smarts-cloud-or-local/>

[马克·韦斯特]在去年的 GOTO Copenhagen 会议上做了一个有趣的报告。他展示了他如何使用一个简单的 Raspberry Pi Zero 网络摄像头，并用人工智能扩展它。他实际上以两种不同的方式添加了智能功能:在亚马逊云上，另一种使用直接连接到 USB 的英特尔 Modvidius NCS USB 棒。你可以看下面的视频。

局部运动检测使用一些开源软件。您只需使用文本文件对其进行配置，它甚至可以处理视频流。然而，在这一点上，你只是有一个网络摄像头-不惊人，也不是很划算。然而，运动检测软件会给你带来很多假警报。一只路过的猫，云，树，甚至雨都会给[马克]发一封电子邮件，在一天 250 封提醒邮件后，[马克]决定做些更好的事情。

【马克的】第一关是用亚马逊的 Rekognition 服务处理视频。这使得摄像机在触发检测事件时变得更加智能。特别是，新相机只有在 Rekognition 看到画面中有人时才会报警。

这很有效，但是以这种方式使用云服务是有成本的。你可能会得到一个免费的试用版，并且有一定程度的免费使用。不过，最终你会为处理的每张图片付费。有了(马克的)四台相机，他最终每月只需支付不到 30 美元。然而，如果他发送更多的图片来提高识别率，成本可能会增加。

当然，没有云也可以进行更复杂的处理。Pi 并不是做神经网络的最佳平台，但是[Mark]发现了 [Intel Movidius 神经计算棒(NCS)。](https://hackaday.com/2018/04/24/neural-networks-on-a-stick/)这款 USB 设备提供了先进的神经网络处理功能，并让 Pi 将大部分工作转移给它。当然，这增加了前期成本，但节省了未来的云费用。它还处理所有帧，而不仅仅是显示变化像素的帧。[Mark]指出，如果谷歌的 Edge TPU 加速器真的上市，它可以完成同样的任务。(编者注:[昨日](https://hackaday.com/2019/03/05/google-launches-ai-platform-that-looks-remarkably-like-a-raspberry-pi/)。)

我们想知道[Mark]是否可以建立自己的私有云，让所有 pi 将数据发送到一个有 NCS 的节点进行处理。我们已经对 NCS 的使用做了自己的尝试。我们还研究了使用 TensorFlow 进行[物体检测。](https://hackaday.com/2018/07/31/object-detection-with-tensorflow/)

 [https://www.youtube.com/embed/lIy9qhwFB-s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lIy9qhwFB-s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

