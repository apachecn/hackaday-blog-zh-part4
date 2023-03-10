# 1000 瓦电源拆除和维修

> 原文：<https://hackaday.com/2018/11/30/1000-watt-power-supply-tear-down-and-repair/>

[TheSignalPath]想要修理一台损坏的 Instek PSW80-40.5，因为它的可编程电源输出功率很大，确切地说是 1080 瓦。这不是一个便宜的供应-它看起来像花费大约 2200 美元新的。这个装置不工作了，当他把它拆开时，他发现了一个令人讨厌的惊喜。有一个基本 PCB 和三个相同的电源模块，如果不断开电路板，几乎无法进入。他[继续拆机](https://www.youtube.com/watch?v=ATYvbKBrmAk)，你可以在下面的视频里看到结果。

每个电源模块都是两个独立的 PCB，设计必须考虑所需的高电流。电源是一个开关设计，在主板上有一些滤波。电源模块的一个板将输入线电压整流为高 DC 电压(大约 400 伏)。然后，第二块板将 DC-DC 转换为所需的输出。

虽然很难找到运行中的电路板，但理论上来说，由于三个模块是相同的，所以应该很容易找出哪个模块是坏的，甚至是模块中两个电路板中的哪一个。这些模块或多或少是自给自足的，尽管有一个控制器要求中央模块提供电压。

首先，他验证了主板上的电压，同时使用隔离变压器来提供低得多的输入电压。然后，他使用主板的一个插槽单独测试了每个模块。

位于中间的电源模块无法启动。它没有任何明显的毛病。然而，对一个良好的模块进行了一点探查和比较，最终发现软启动电路中有一个故障电阻。

他用一个类似的装置暂时分流了开路电阻，使模块开始工作。不过，这还不是结局。另一个模块上有一些烧伤的痕迹。该区域靠近 MOSFET 附近的一些非常低值的电阻。该电路有一个不错的保险丝，但看起来好像当 FET 短路时，电阻可能在保险丝之前熔断。

我们很高兴看到其他人堆叠 SMD 电阻来并联它们。我们现在不觉得这样做很尴尬了。我们也喜欢所有的*特别*电路分析，因为没有可用的原理图。

虽然电源的内部很紧凑，但它没有我们享受的那种[光芒。它看起来确实比我们拆掉的](https://hackaday.com/2018/09/08/a-switching-power-supply-1940s-style/)[廉价电源](https://hackaday.com/2015/10/15/looking-inside-the-arksen-dual-power-supply/)更好，因为它关闭时会杀死模块。

 [https://www.youtube.com/embed/ATYvbKBrmAk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ATYvbKBrmAk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

