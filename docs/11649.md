# 二极管是开关吗？

> 原文：<https://hackaday.com/2021/10/24/is-a-diode-a-switch/>

这些部件周围的许多硬件人员将熟悉用作开关的设备，使用至少三个端子来实现这一点，一个输入、一个输出和一个门。浮现在脑海中的典型器件有双极晶体管、三端双向可控硅开关和老式三极管开关。即使只有两个端子，你能使用二极管来切换信号吗？[当然可以](https://www.youtube.com/watch?v=NJuoHVX2htA)，这是一种久经考验的可靠技术，在处理 RF 信号的测试设备和电路中非常常见。(视频，嵌在下面。)

诀窍在于，二极管在一个方向上阻挡电流，但允许电流在另一个方向上流动，这一点由特意设计的明显符号表示。所以你的 DC 信号不能逆流而上，但同样的情况不适用于交流电。通过感应电流的微小波动，信号可以“错误地”通过二极管。换句话说，如果将二极管偏置为导通状态，下游电压电平的变化会导致流经二极管的电流发生变化，从而让(较小的)交流信号通过。但是，如果通过关闭 DC 偏置电压源来消除偏置，二极管就会切换回非导通状态，从而阻断信号。这使得二极管成为交流信号的 DC 控制开关。

虽然[IMSAI Guy]用信号二极管证明了这一点，但他解释说，人们通常会使用 PIN 二极管，它在 P 和 N 之间有一个额外的本征(未掺杂)区，允许器件完全关断，从而显著降低泄漏。

当然，我们已经从不同角度多次讨论过二极管，总有一些东西需要学习。查看如何构建[高压二极管](https://hackaday.com/2021/10/03/what-goes-into-a-high-voltage-diode/)、[检测电离辐射的二极管](https://hackaday.com/2021/10/03/what-goes-into-a-high-voltage-diode/)，最后是关于我们最喜欢的双端设备的[大系列。](https://hackaday.com/2019/11/11/diode-basics-by-w2aew/)

看吧，不起眼的二极管终究可以好玩！

 [https://www.youtube.com/embed/NJuoHVX2htA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NJuoHVX2htA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[真相]的提示！