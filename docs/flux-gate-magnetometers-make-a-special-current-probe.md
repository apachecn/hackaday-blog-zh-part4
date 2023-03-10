# 磁通门磁力计是一种特殊的电流探头

> 原文：<https://hackaday.com/2019/09/21/flux-gate-magnetometers-make-a-special-current-probe/>

有些时候，需要对既不能断开以插入串联电阻，也不能用电流互感器环绕的导体进行电流测量。这些测量需要完全非侵入性的技术，为了满足这种需求，有商业磁力计电流探头。然而，这些探测器不是为了钱包的光，所以[ensgoldmine] [创造了一个更便宜的替代品](https://hackaday.io/project/167634-drv425-fluxgate-magnetometer-based-current-probe)。

TI 评估模块上的[德州仪器 GRV425](http://www.ti.com/product/DRV425#) 磁通门磁力计集成电路将测量元件放置在探头尖端，尽可能靠近待测导体，探头头部的另一个 GRV425 模块用于测量环境磁场以进行校准。Arduino Due 测量和处理读数，选择 Arduino Due 是因为它的 ADC 分辨率比更普遍的 Arduino Uno 高。

即使你不需要电流探头，这篇文章也很有趣，因为它引入了这些传感元件。因为这对于黑客来说是罕见的第一次，我们之前从未近距离观察过它们，除了在谈论火星上的科学仪器时作为一个题外话。