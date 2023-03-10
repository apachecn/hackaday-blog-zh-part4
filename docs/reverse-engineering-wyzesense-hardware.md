# 逆向工程 WyzeSense 硬件

> 原文：<https://hackaday.com/2019/06/11/reverse-engineering-wyzesense-hardware/>

Wyze 是一家生产各种家庭自动化产品的公司。他们的 Wyze Sense 包是一个接触和 PIR 家庭安全传感器系统，它依赖于他们的 Wyze Cam 产品。为了能够在规定的企业生态系统之外使用这些硬件，[【星璇】开始着手黑客行动。](https://hclxing.wordpress.com/2019/05/30/reverse-engineering-wyzesense-bridge-protocol-part-i/)

该项目首先拆除 Wyze 摄像头，并获得串行控制台访问。现有的 Github 项目[使这变得更加容易，该项目为智能相机开发定制固件。有了这个，他就能看到引擎盖下发生了什么，并读取相机的系统日志。](https://github.com/EliasKotlyar/Xiaomi-Dafang-Hacks)

通过研究这些日志，并检查拆卸的 Wyze Sense dongle，他正在探索传感器如何与 Wyze Cam 通信。最终目标是使 Wyze 安全传感器能够与 Raspberry Pi 平台一起使用，并在 Github 上共享代码，供其他制造商进行试验。

家庭自动化平台来来去去比季节变化还快。这使得硬件成为黑客们的热门目标，他们试图让硬件独立于任何一家公司的服务器运行。