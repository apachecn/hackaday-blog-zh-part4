# 有弹性的人工智能无人机将所有东西都包装在 250 克以下

> 原文：<https://hackaday.com/2021/03/15/resilient-ai-drone-packs-it-all-in-under-250-grams/>

当首次宣布对重量超过 250 克的休闲遥控飞机进行限制时，许多人认为新规则意味着家用四轴飞行器的终结。但是制造商们奋起迎接挑战，开始开发难以置信的小而轻的硬件版本。今天，用第一人称视角(FPV)相机建造和飞行超轻量级四轴飞行器已经成为一种专门的爱好。

但是，尽管那些轻量级飞行员可能令人印象深刻，CogniFly 项目确实推动了我们在这个重量级中认为可能的事情。这款开源四轴飞行器旨在作为人工智能无人机的实验平台，它搭载了 Raspberry Pi Zero 和谷歌的 AIY 视觉套件，因此它可以在空中执行复杂的计算任务，如图像识别。为了防止这些实验发生意外，它还被封装在一个独特的柔性框架中，使其对碰撞损伤具有极强的弹性。正如你在休息后的视频中看到的那样，即使直接撞上了一堵墙，CogniFly 也可以继续前进，就像什么都没发生过一样。

在电平转换器的帮助下，Raspberry Pi 可以通过 UART 与四轴飞行器的飞行控制器直接通信。CogniFly 团队开发的 [Python 库允许 Pi 使用 MSP (MultiWii 串行协议)向飞行控制器发出命令，当与其他机载传感器结合起来检测高度和相对运动时，这意味着人类飞行员几乎没有什么可做的了。](https://github.com/thecognifly/YAMSPy)

[![](img/92f79cb33f6c6d63f4b9531a70fb0e00.png)](https://hackaday.com/wp-content/uploads/2021/03/cognifly_detail.jpg)

3D printed TPU connectors

CogniFly 被包裹在一个独特的框架中，不仅保护了所有的高科技设备，还确保了旋转的螺旋桨与边缘保持足够的距离，不会在碰撞中撞到任何东西(或任何人)。该团队没有完全采用刚性材料，而是想出了一种巧妙的建造技术，将柔性 TPU 连接器与碳纤维棒结合起来。

TPU 作品可以在廉价的 3D 打印机上打印出来，然后折叠起来进行组装。如果任何一个框架部件在特别剧烈的撞击中损坏，可以在现场用少量的备用零件快速容易地修复。

展望未来，该团队已经以这样一种方式设计了框架，即 CogniFly 将能够在需要新电池包时降落在旋转电池更换器上。在黑客和制造商生态系统中，没有太多关于[自动电池交换的现有技术，鉴于他们的概念是多么雄心勃勃，我们非常有兴趣看看该项目的这一要素如何进展。](https://hackaday.com/2016/11/30/where-is-my-drone-ask-lighthouse/)

对于任何想要尝试自主飞行的人来说，CogniFly 都是一个特别引人注目的平台，而且它足够轻，可以绕过大多数无人机法律，这对于爱好者来说是一个巨大的优势。你可能会认为，到 2021 年，我们已经看到了所有可以想象的四轴飞行器，但偶尔仍会出现新的设计，这证明仍有很大的创新空间。

 [https://www.youtube.com/embed/Y_Z54x4MjoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y_Z54x4MjoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

