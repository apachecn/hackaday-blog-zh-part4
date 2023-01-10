# 用第一个开源 PDK 创建定制 ASIC

> 原文：<https://hackaday.com/2020/06/25/creating-a-custom-asic-with-the-first-open-source-pdk/>

工艺设计工具包(PDK)是目前将新芯片设计转化为硅芯片的相当标准的一部分。PDK 描述了设计如何映射到代工厂的工具，代工厂本身由 DRM 或设计规则手册描述。FOSSi 基金会[现在报道](https://fossi-foundation.org/2020/06/17/fossi-dial-up)由谷歌和 SkyWater Technology 发起的一个新的、开放的 PDK 项目。虽然 [OpenPDK 项目](https://www.eetimes.com/globalfoundries-joins-openpdk-group/)已经存在了一段时间，但它是一个封闭的、高度专有的系统，面向制造商和代工厂。

Github 上的 [SkyWater 开源 PDK](https://github.com/google/skywater-pdk) 被列为谷歌和 SkyWater Technology Foundry 之间的合作，旨在提供完全开源的 PDK 和相关源代码。这使得人们可以在 SkyWater 铸造厂创建可制造的设计，目标是 130 nm 节点。这里的开放工具应该意味着比通常情况下低得多的进入成本。

虽然这是一个相当老的工艺节点(大约 19 年)，但它对一系列应用仍然非常有用，尤其是那些合并数字和模拟电路的应用。SkyWater 列出了他们的 SKY130 节点技术体系:

*   支持内部 1.8V 和 5.0V I/o(可在 2.5V 下工作)
*   1 级本地互连
*   5 级金属
*   支持电感的
*   高薄层 rho 多晶电阻器
*   可选 MiM 电容
*   包括 SONOS 缩小细胞
*   支持 10V 稳压电源
*   高压扩展漏极 NMOS 和 PMOS

应该注意的是，这个开源 PDK 的使用在这个时候被认为是实验性的，不应该用于任何商业或其他敏感的应用。

标题图像:Peellden/ [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:12-inch_silicon_wafer.jpg)