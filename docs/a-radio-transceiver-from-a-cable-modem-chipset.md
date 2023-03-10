# 电缆调制解调器芯片组的无线电收发器

> 原文：<https://hackaday.com/2019/08/31/a-radio-transceiver-from-a-cable-modem-chipset/>

让电子设备做制造商从未为它们设计的事情，是我们社区工作的主要内容。例如，使用 CMOS 逻辑芯片的模拟合成器，或者无需 MAC 硬件就能处理以太网数据包的微控制器。该领域最吸引人的地方之一是软件定义无线电(SDR ),我们中很少有人不拥有一台基于 RTL2832 的数字电视接收机，它被用作 SDR 接收机。

不过，RTL SDR 并不是唯一的例子，因为有一整类电缆调制解调器芯片组都包含基本的 SDR 构建模块。 [Hermes-Lite](http://www.hermeslite.com/) 是一个 HF 业余无线电收发器项目，使用 AD9866 电缆调制解调器芯片作为其 12 位 SDR 收发器硬件的信号端，在它与以太网接口之间有一个 FPGA。它覆盖从 0 到 38.4 MHz 的频率，具有 384 kHz 的带宽，并可以收集高达 5W 的输出功率。

这是一个在过去几年中一直在我们的雷达上的项目，尽管有点令人惊讶的是这是在 Hackaday 上第一次提到它。创建者[Steve Haynal]提醒我们，第二版现在已经是第九次迭代的成熟项目，并说迄今为止已经组装了超过 100 个“Hermes-Lite 2.0”单元。如果你想要一个自己的爱马仕 Lite，它是完全开源的，他们组织所需组件的团购。

当然，由意想不到的组件[制成的 SDR 不一定是奇异的](https://hackaday.com/2018/12/06/your-usb-serial-adapter-just-became-a-sdr/)。