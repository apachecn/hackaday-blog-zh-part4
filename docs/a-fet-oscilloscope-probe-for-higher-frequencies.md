# 高频 FET 示波器探头

> 原文：<https://hackaday.com/2022/04/23/a-fet-oscilloscope-probe-for-higher-frequencies/>

自从第一批电子沿着导线被传送以来，这个问题就一直困扰着电子工程师:测量仪器本身会扰乱电路的运行。例如，老式万用表的阻抗低到足以拉电阻值，因此我们今天的万用表具有高阻抗 FET 输入。[Christoph]用他的示波器探头面对它，它的输入电容高到足以给晶体振荡器带来不可接受的负载，使其停止振荡。因此，他为更高的 RF 频率构建了[FET 输入探针，其构建是宽带 RF 仪器设计的一个可访问视图。](https://hackaday.io/project/184924-diy-13-ghz-fet-probe)

该电路非常简单，使用双栅极 FET，但人们感兴趣的是 PCB 和屏蔽设计，以确保良好的 RF 性能。现成的易拉罐有四个侧面，因此为了容纳电路，必须拆除易拉罐的一个侧壁。最终结果是[一个微型 PCB](https://github.com/crteensy/FETProbe_tiny) ，带有用于电源和信号的微型同轴连接器，其特征是具有 1.3 GHz 带宽和非常低的输入电容。

如果 RF 设计语言对您来说很陌生，我们可以推荐几年前[【Michael OSS Mann】在超级会议上的演讲](https://hackaday.com/2016/03/23/michael-ossmann-makes-you-an-rf-design-hero/)。