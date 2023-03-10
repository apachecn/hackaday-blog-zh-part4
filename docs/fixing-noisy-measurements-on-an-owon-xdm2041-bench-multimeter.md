# 修复 Owon XDM2041 台式万用表上的噪声测量

> 原文：<https://hackaday.com/2021/07/14/fixing-noisy-measurements-on-an-owon-xdm2041-bench-multimeter/>

在购买了 Owon XDM2041 台式万用表用于自动测试设置后，[Petteri Aimonen]失望地发现，尤其是在更高的兆欧范围内，测量值波动很大，而且通常非常不准确。由于这是一个大约 170 美元的台式万用表，Owon support 不配合，[Petteri] [着手解决问题](http://essentialscrap.com/owon_fix/)，从彻底拆卸开始。

[![](img/b8476233b7646dd8d74546cd822009b7.png)](https://hackaday.com/wp-content/uploads/2021/07/resistance_noise.png) 正如【佩特里】所指出的，在这些万用表中没有一个完整的批次。主板是整个系统的核心，它包含一个 GigaDevices GD32F103CBT6 MCU，再加上展会的明星:HYCON Technology Corporation 的 [HY3131](https://www.hycontek.com/wp-content/uploads/DS-HY3131_EN.pdf) 万用表芯片。查看 HY3131 数据手册后，问题很明显:在采样时，通常通过选择合适的晶体来抑制电源电压噪声。

不幸的是，Owon 的工程师显然没有选择 HY3131 参考原理图中推荐的 4.9152 MHz 晶体，而是选择了 4 MHz 晶体，因此实际上是[混淆了线路噪声](https://hackaday.com/2017/03/23/say-it-with-me-aliasing/)。

[Petteri]认为，对于 60 Hz 线路频率，由此产生的采样时序可能足够好，但对于 50 Hz，显然会有大量噪声混入测量结果。将晶体换成 3.072 MHz 后，有了明显的改善，如图所示。