# 一片 FPGA 和几个元件就可以做成一台收音机

> 原文：<https://hackaday.com/2020/04/18/an-fpga-and-a-few-components-can-make-a-radio/>

曾经有一段时间，制造无线电接收器需要大量的工作，大量的线圈缠绕，以及电路的复杂调整。软件定义无线电(SDR)的出现将许多这种技术转移到了软件领域，但当然还有另一个领域可以通过代码创建无线电。[ Alberto Garlassi ]已经[用点阵 MachXO2 FPGA](https://hackaday.io/project/170916-fpga-3-r-1-c-mw-and-sw-sdr-receiver) 和最少的外部元件制造了一个 AM 和 HF 波段的无线电接收机。

他将其描述为 SDR，鉴于它是由 Verilog 创建的，这个术语可以用来形容它。但它没有使用 ADC 和数字信号处理的 SDR 拓扑结构，而是实现了一个令人惊讶的传统直接变频接收机。

它有一个正交 AM 解调器，与具有 I 和 Q 相位信号的 SDR 有一定的相似性，但相似性仅此而已。频率选择是通过串行端口控制的振荡器实现的，甚至还有一个 PWM 放大器可以驱动扬声器。结果可以在下面的视频中看到，正如您所听到的，采用正交解调器的直接变频方法是一种非常有效的 AM 接收机。

如果这有点多，但你仍然喜欢最小组件的收音机，你应该[看看硅实验室的接收器芯片系列](https://hackaday.com/2020/03/02/multi-band-receiver-on-a-chip-controlled-by-arduino/)。

 [https://www.youtube.com/embed/Dde6-o0uda0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Dde6-o0uda0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

