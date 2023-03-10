# DIY 步进衰减器，将两个较小的衰减器粘合在一起

> 原文：<https://hackaday.com/2019/06/04/a-diy-step-attenuator-by-gluing-together-two-smaller-ones/>

在射频领域，衰减器是一种有用的测试和测量工具。可以在离散步骤中应用不同衰减水平的可变单元甚至更好。[DuWayne]通过将两个较小的单元串联在一起制作了一个 63 dB 的步进衰减器，由 Arduino Nano 控制它们。凭借 3D 打印外壳和反馈有机发光二极管，该设备可通过单个旋转编码器轻松调节。甚至还有空间添加一个微型 USB 插头来为电源充电。

使用的两个较小的数字衰减器[DuWayne]基本上是 PE4302 数字 RF 衰减器的分线板，可以从通常的海外来源廉价获得。它们能够以 0.5 dB 的步长实现高达 31.5 dB 的衰减，通过串联使用两个(并并联控制)[DuWayne]获得高达 63 dB 的范围。设计文件[可以从项目的 Dropbox 共享目录](https://www.dropbox.com/sh/2ymaiyxjt1bagwq/AAAVxnZWWdequNoA7kLNuR5Ra?dl=0)下载，如果你想自己尝试的话。

您对 RF 或者软件无线电(SDR)感兴趣吗？我们已经涵盖了[你开始使用廉价 RTL-SDR](https://hackaday.com/2018/11/09/all-the-goodies-you-need-for-your-rtl-sdr/) 所需的所有材料，迟早你会发现自己需要[【丹·马洛尼】关于廉价有效假负载的信息](https://hackaday.com/2019/04/25/the-50-ham-dummy-loads/)。