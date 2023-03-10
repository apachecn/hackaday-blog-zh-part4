# 低成本双通道脚本化波形发生器

> 原文：<https://hackaday.com/2022/03/05/low-cost-two-channel-scriptable-waveform-generator/>

微控制器爱好者[Debraj]决定制作自己的可编程正弦波发生器，并且能够以不到 40 美元的价格组装起来。除了低成本，他的需求列表如下:

*   双正弦波输出，同步
*   频率、幅度和相位控制
*   1 MHz 以下的低谐波
*   可通过 Python 编写脚本

该项目的核心是 ADI 公司的[ad 9833](https://www.analog.com/media/en/technical-documentation/data-sheets/ad9833.pdf)，这是一款片上完整的直接数字频率合成(DDS)波形发生器系统。如果您曾经使用分立式 ic 或在 FPGA 中实现过自己的 DDS，您会体会到将相位累加器、正弦查找表、DAC 和控制逻辑集成到一个 10 引脚封装中的好处。[Debraj]使用常见在线供应商提供的 AD9833 模块，每个售价几美元。他通过断开第二个模块上的参考晶体并从第一个模块驱动它来同步发电机。其余规格由 DDS 系统的固有特性来满足，可编写脚本的接口通过一个 Arduino 控制 AD9833 芯片和两个可编程增益放大器( [MCP6S31](http://ww1.microchip.com/downloads/en/devicedoc/21117b.pdf) )来实现。我们喜欢[Debraj]用圆珠笔画出初始电路图所展示的自信——请看视频中休息处下方的草图和最终示意图。

这是一个结合现成模块快速构建项目的好例子。这种方法非常适合一次性构建，或者作为概念验证测试平台，稍后可以旋转到定制 PCB 上。如今使用模块的另一个原因是，模块通常有现货，但芯片却买不到。虽然看起来[Debraj]只需要其中一台发电机，但如果你能买到零件，这将是一个很容易布局和建造的电路板。

 [https://www.youtube.com/embed/ODtvqU939jw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ODtvqU939jw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

