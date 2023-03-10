# 半刚性同轴电缆和 SDR 的 DIY EMC 探头

> 原文：<https://hackaday.com/2019/04/24/a-diy-emc-probe-from-semi-rigid-coax-and-an-sdr/>

您的工具包中有 EMC 探头吗？可能不会，除非你从事电磁兼容性测试的业务，或者为法规遵从性过程准备好产品。通常这种探头用在消声室中，并连接到频谱分析仪等复杂的设备上——这是很昂贵的东西。但是有很多方法可以廉价地探索你的项目的电磁奥秘，正如这个 DIY 的 EMC 测试装置所证明的。

与许多项目一样，[dimtass]的制作灵感来自 EEVblog 上的一个视频，其中[Dave]用一段半刚性同轴电缆制作了一个简单的 EMC 探头。10 美元，这是一个便宜的解决方案，但缺乏像[戴夫]插入他的廉价探针的频谱分析仪，[dimtass]走了一条不同的路。通过将自制的探针插入 RTL-SDR 加密狗和在 PC 上运行的 SDR #,[ dim tass]能够获得一个相当接近频谱分析仪的结果，至少在对 10 MHz 恒温晶体振荡器进行测试时是如此。它与专用频谱分析仪不是一回事——带宽有限、噪声更高、未经校准——但它工作得足够好，而且正如[dimtass]指出的那样，可以通过 SDR# API 无限破解。当探头直接插入一个运行 FFT 功能的 DSO 时，它甚至可以正常工作。

同样，这两种设置都不能替代适当的 EMC 测试，但它可能适合家庭游戏玩家。如果你想了解专业人员为确保他们的产品不会发出信号所做的努力，请查看[【Jenny】对 EMC 测试流程的概述](https://hackaday.com/2017/02/20/an-overview-of-the-dreaded-emc-tests/)。

[via[RTL-SDR.com](https://www.rtl-sdr.com/creating-an-emc-probe-using-an-rtl-sdr-and-semi-rigid-coax/)