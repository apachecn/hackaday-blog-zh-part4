# 谷歌推出人工智能平台，看起来非常像树莓派

> 原文：<https://hackaday.com/2019/03/05/google-launches-ai-platform-that-looks-remarkably-like-a-raspberry-pi/>

谷歌向我们承诺了机器学习的新硬件产品，现在终于发布了。你将从这里学到的是，谷歌用机器学习建立了一个树莓派。这是谷歌的 Coral，带有 Edge TPU 平台，这是一种定制的 ASIC，旨在“在边缘”运行机器学习算法。[这是链接](https://coral.withgoogle.com/products/dev-board/)到看起来像树莓派的电路板。

这款新硬件在 TensorFlow 开发峰会之前推出，围绕嵌入式应用中的机器学习和“人工智能”，特别是功率和计算受限的环境。这是营销术语中的“边缘”,我们已经看到了一些从头开始设计的产品，用于在嵌入式应用中运行 ML 算法和推理。现在有带机器学习加速器的 RISC-V 微控制器可用， [Nvidia 已经在这方面工作了多年](https://hackaday.com/2017/03/14/hands-on-nvidia-jetson-tx2-fast-processing-for-embedded-devices/)。现在，谷歌推出了一款定制设计的 ASIC 来加速 TensorFlow。碰巧棋盘看起来像树莓皮。

## 黑板上有什么

Coral dev 板上有一个恩智浦 i.MX 8M SOC，配有一个四核 Cortex-A53 和一个 Cortex-M4F。GPU 被列为“集成 GC7000 Lite 显卡”。RAM 为 1gb lpddr 4，Flash 提供 8GB eMMC，包含 WiFi 和蓝牙 4.1。连接通过 USB 提供，带有 C 型 OTG、C 型电源连接、A 型 3.0 主机和 micro-B 串行控制台。千兆以太网、3.5 毫米音频插孔、麦克风、全尺寸 HDMI、4 通道 MIPI-DSI 和 4 通道 MIPI-CSI2 摄像头支持。GPIO 引脚完全——我的意思是*完全*——就像 Raspberry Pi GPIO 引脚。GPIO 引脚在相同的位置提供相同的信号，尽管由于不同的 SOC，您需要更改一两行定义引脚编号的代码。

你可能会问为什么谷歌会制造一个树莓派的克隆版。答案是在主板上植入一个机器学习加速器芯片。机器学习和人工智能芯片在 80 年代很流行，我想一切旧的都是新的。谷歌 Edge TPU 协处理器支持 [TensorFlow Lite](https://www.tensorflow.org/lite) ，即“边缘的机器学习”。TensorFlow Lite 的目的不是*训练*一个系统，而是运行一个现有的模型。它会进行面部识别。

Coral dev 板售价 149.00 美元，您可以在 Mouser 上订购。截至本文撰写时，[Mouser 订购了 1320 台，交付日期为 3 月 6 日](https://www.mouser.com/ProductDetail/Coral/G950-01455-01?qs=sGAEpiMZZMtw0nEwywcFgJjuZv55GFNmP%252BfgDTXLnZ%252B5XIZ6VY5BuA%3D%3D)(搜索 Mouser 零件号 212-193575000077)。

## 也是加密狗形式

![](img/7477996a6eec23ba397bfd22508d7818.png) [硬件组合中还有另一个设备](https://coral.withgoogle.com/products/accelerator/)，叫做 USB 加速器，我们只能假设是连接到 USB 电缆的 Edge TPU。这个 USB 加速器将与 Raspberry Pi 一起工作——顺便说一下，这是谷歌的产品副本——并将让你开始使用谷歌设计的 Edge TPU 进行机器学习推理。这个 USB 加速器的价格是 75 美元。

我们要祝贺 Raspberry Pi 基金会创造了如此无处不在的东西，甚至谷歌都觉得有必要搭上它的顺风车。