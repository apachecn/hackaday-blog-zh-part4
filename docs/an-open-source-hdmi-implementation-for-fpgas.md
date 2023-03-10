# 一种面向 FPGAs 的开源 HDMI 实现

> 原文：<https://hackaday.com/2020/06/02/an-open-source-hdmi-implementation-for-fpgas/>

通过一些巧妙的技巧和快速的 IO 工作，让普通的微控制器输出某种形式的视频是可能的。像 composite 和 VGA 这样的老模拟标准速度很慢，很有可能一蹴而就。然而，如果你对视频工作很认真，你会想要更有能力的东西。对于这些用例，[purisame]提供了您所需要的—[面向 FPGAs 的开源 HDMI 实施方案。](https://github.com/hdl-util/hdmi/)

与这个领域的其他自由和开源项目不同，[purisame]避免了简单地在端口上输出兼容的 DVI 信号。这种实现是纯 HDMI 1.4b，支持由此带来的扩展功能，如组合视频和音频流。到目前为止，它已经在 Xilinx 和 Altera 平台上进行了测试，尽管它也可能与 Lattice 兼容。

除了代码之外，[purisame]还为那些希望将 HDMI 设备投入生产的人提供了一些选择。销售技术的许可可能是一个令人担忧的领域，所以如果你要去市场，建议找个律师。哦，有趣的是，如果你真的想在 Arduino 上做 HDMI，[也有一个屏蔽。当然。](https://hackaday.com/2019/07/26/hdmi-from-your-arduino/)