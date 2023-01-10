# 专为机器学习设计的 RP2040 板

> 原文：<https://hackaday.com/2021/04/13/an-rp2040-board-designed-for-machine-learning/>

机器学习(ML)通常会想到需要大量存储和大量处理能力的花哨代码。然而，有一些 ML 模型，一旦经过训练，就可以在更加简单的硬件上运行——甚至是微控制器！Raspberry Pi Pico 的明星产品 RP2040 就是这样一款芯片，[和[Arducam]已经宣布了一款旨在实现这些目标的主板 Pico4ML。](https://www.arducam.com/pico4ml-an-rp2040-based-platform-for-tiny-machine-learning/)

该板在硬件上很重，为 RP2040 配备了大量对机器学习任务有用的工具。板上有一个 QVGA 摄像头，以及一个 0.96 英寸的 TFT 显示屏。如果需要的话，甚至可以将摄像机画面直播到屏幕上。还有一个捕捉音频的麦克风和一个 IMU，已经烘焙到板上。这使得物体、语音和手势识别完全在 Pico4ML 的权限之内。

在 Pico4ML 这样的主板上运行 ML 模型并不是为了实现健壮的高性能。相反，它是为低功耗和便携性是关键的应用而设计的。如果你对 Pico4ML 能做什么和做得好有什么想法，请在评论中发表。我们可能会把它连接到一个网络上，这样当我们喊着要披萨的时候，它就可以自动下订单了。我们之前也讨论过微控制器上的机器学习——[一个关于如何开始的精彩 Remoticon 演讲！](https://hackaday.com/2020/12/04/remoticon-video-how-to-use-machine-learning-with-microcontrollers/)