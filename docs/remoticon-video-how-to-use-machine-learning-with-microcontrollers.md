# Remoticon 视频:如何在微控制器上使用机器学习

> 原文：<https://hackaday.com/2020/12/04/remoticon-video-how-to-use-machine-learning-with-microcontrollers/>

从一个闪烁 LED 的微控制器，到一个基于你在神经网络上训练的数据集使用语音命令闪烁 LED 的微控制器，是一个“现在画出猫头鹰的其余部分”的问题。幸运的是，Shawn Hymel 在他的 2020 Hackaday Remoticon 小型 ML 工作室中向我们展示了整个过程。该视频刚刚发布，可以在下面观看。

对于在微控制器上启动和运行机器学习来说，这是一个真正的端到端 Hello World。Shawn 介绍了收集和准备音频样本、训练数据集以及将所有这些内容输入微控制器的过程。两个小时后，他能够展示 STM32 识别并回应两个不同的口语单词。在这个过程中，他会停下来讨论每一步中发生的事情的背景，这将有助于您在以后返回并扩展这些领域，以满足您自己的项目需求。

 [https://www.youtube.com/embed/iO7_qr9s3lw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iO7_qr9s3lw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



本演示中使用的硬件是 STM32 Nucleo-L476RG 板，但您也可以在各种 ARM 板和其他合适的高性能芯片上使用相同的技术。

硬件要求在车间项目页面的[中有详细说明。肖恩在他的 GitHub repo](https://hackaday.io/project/175078-remoticon-tiny-ml)上收集了[一些史诗般的文档，包括研讨会的幻灯片。自视频录制以来，他甚至用 Arduino Nano 33 BLE 感应板](https://hackaday.io/project/175078-remoticon-tiny-ml)为[制作了一个演示，该感应板使用了一个北欧 nRF52480 芯片。](https://github.com/ShawnHymel/ei-keyword-spotting/tree/master/embedded-demos)

研讨会的大部分时间花在研究用于训练数据集的软件平台和设置的迷宫上。一个有趣的 Jupiter 笔记本演示收集和整理了 120 分钟的 1 秒钟音频样本用于培训。还有另外 20 分钟的测试数据—这些样本不在训练集中，将用于验证以前未知的输入是否可以成功分类。

训练过程本身是在一个叫做 [Edge Impulse](https://www.edgeimpulse.com/) 的平台上运行的。这提供了一个图形 web 界面，用于汇集训练集使用的参数。在这种情况下，音频样本被转换成[梅尔倒谱系数](https://en.wikipedia.org/wiki/Mel-frequency_cepstrum) (MFCCs)并被馈入 [Keras](https://keras.io/about/) 神经网络。(在研讨会的后期，Shawn 谈到了一旦您开始熟悉整个设置，如何调整 Keras 代码。)微控制器会将每个输入的音频样本实时转换为 MFCC，可以与 Edge Impulse 以 C 包形式输出的数据集进行比较。

他让它看起来很简单，你绝对应该试一试。同时，这也是一个很好的例子，说明为什么记录你的项目，即使只是个人使用，是如此重要。我们很高兴有 Shawn 的一步一步指导，但即使是他，在将数据集导入 STM32CubeIDE 软件时也会引用它。