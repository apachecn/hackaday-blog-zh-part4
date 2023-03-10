# MIPI CSI-2 在 FPGAs 中的实现

> 原文：<https://hackaday.com/2018/11/29/mipi-csi-2-implementation-in-fpgas/>

[Adam Taylor]总是有有趣的 FPGA 帖子，他的最新帖子也不例外。他想用 Zynq 进行图像处理。有道理。可以在 FPGA 结构中做高速并行部分，在内置 CPU 上做更高级的处理。问题是，当然，你需要把视频数据输入系统。[Adam]选择使用[移动工业处理器接口(MIPI)摄像机串行接口问题 2 (CSI-2)](https://blog.hackster.io/microzed-chronicles-working-with-mipi-b16b67990ccc) 。

这种高速串行接口针对单向数据流进行了优化。摄像机或主机用一个时钟连续发送许多位(至少一位)。为了提高速度，数据在时钟上升沿和下降沿传输。从机也有一个非常标准的 I2C 主机向摄像机发送命令，对于 I2C 来说，它就是从机。

理论上，对于 D-PHY 上的一个通道的数据，你可以在四条线上获得高达 4.5 Gbps 的速度，尽管用 FPGA 可能会更低。[Adam 的]帖子引用了不同的数字，但也提到 FPGA 无论如何也达不到目标。所使用的芯片之一直接在芯片上支持 D-PHY，但标准的 Zynq 不支持。即使在使用 IP 时，你也必须理解这一点，并做出适当的选择，这是本文的要点。

它确实说明了即使使用 IP 也不如连接家庭立体声设备那样即插即用。您仍然需要了解发生了什么，以及如何最好地使用 IP——在这种情况下，既要了解外部接口，也要了解内部接口。

如果您想在 FPGA 上查看更简单的串行接口，请尝试我们的 [POV 项目](https://hackaday.com/2018/09/06/fpga-pov-toy-gets-customized/)。我们还使用了一个类似的串口来伪造[一个内部逻辑分析仪](https://hackaday.com/2018/10/12/logic-analyzers-for-fpgas-a-verilog-odyssey/)。