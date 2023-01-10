# 3D 打印的风扇支架使服务器 GPU 在台式机机箱中保持凉爽

> 原文：<https://hackaday.com/2021/11/06/3d-printed-fan-mount-keeps-server-gpu-cool-in-desktop-case/>

Hackaday 的大多数读者都很清楚目前半导体，尤其是 GPU 的短缺。无论你是计划建造一台最先进的游戏 PC，一个将你的千瓦时转换为加密硬币的采矿钻机，还是只是在试验机器学习人工智能，你都应该准备好为一个合适的 GPU 支付比过去好的多得多的钱。

不过，在二手市场上仍然可以买到便宜货。[Devon Bray]偶然发现了一对 Nvidia Tesla K80 卡，它们不适合游戏，对于挖掘密码来说也不再具有成本效益，但对于[Devon]的机器学习计算来说是理想的。然而，他不得不做了一个[修改，以实现适当的热量管理](https://www.esologic.com/tesla-cooler/)，因为这些卡不是为普通台式电脑设计的。

这是因为许多专业级 GPU 加速器安装在机架式服务器机箱中，因此配备了散热器，但没有风扇:机箱旨在提供强制气流，带走卡的热量。简单地将卡安装到桌面 PC 机箱中会导致它们过热，因为被动冷却不会消除每张卡在满载时产生的 300 W 功率。

[Devon]决定通过 3D 打印一个支架来制作一个合适的散热解决方案，该支架带有三个风扇以及一个卡在 GPU 卡上的空气导管。为了防止不必要的风扇噪音，他添加了一个热控制系统，由一个树莓 Pi Pico，几个 MOSFETs 和一个热敏电阻组成，以感应 GPU 的温度，因此只有当卡变热时才会驱动风扇。Pi Pico 当然比完成这样一个简单的任务所需的更强大，但是允许[Devon]在 MicroPython 中编程，使用比 Arduino 更先进的编程技术。

我们喜欢风扇导管的优雅设计，这使得两个这些巨大的卡能够并排安装到主板上。我们已经看到有人致力于解决相反的问题[将大风扇装进小盒子](https://hackaday.com/2020/07/10/hacked-case-fan-follows-the-leader-with-ir-sensor/)，以及[放弃使用风扇](https://hackaday.com/2021/07/06/bellow-cooled-pc-is-a-well-engineered-display-piece/)冷却的整个想法的设计。

 [https://www.youtube.com/embed/ax6S3I81yAg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ax6S3I81yAg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

