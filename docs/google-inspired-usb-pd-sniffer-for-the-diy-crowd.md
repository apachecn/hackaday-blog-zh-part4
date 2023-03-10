# 谷歌启发的 USB-PD 嗅探器，适合 DIY 人群

> 原文：<https://hackaday.com/2021/02/20/google-inspired-usb-pd-sniffer-for-the-diy-crowd/>

如果你想破解 USB 电力传输设备用来与上游电源协商电力需求的通信协议，像谷歌的 Twinkie 这样的工具真的很有帮助。有了它，你可以嗅出线外的数据，分析它，甚至注入你自己的包。对我们来说幸运的是，搜索巨头将该设备开源，所以我们都可以有一个自己的设备。

不幸的是，正如[dojoe]发现的那样，Twinkie 并不特别适合小规模的业余制作。因此，他提出了一个被他称为 Twonkie 的修订设计，用一个更合理的四层版本取代了六层 PCB，这种版本可以由 OSHPark 以更低的成本制造，并用你可以手工焊接的 QFP 替代品替换 BGA 元件。

尽管如此，对于家庭游戏玩家来说，这仍然是一个具有挑战性的版本。有相当多的 0402 钝化在那里，虽然这些是可行的与铁，[它肯定可以棘手](https://hackaday.com/2019/11/18/a-newbie-takes-the-smd-challenge-at-supercon/)。为了减轻一些压力，[dojoe]说他试图尽可能地优化手工组装的电路板布局。他甚至能够通过将 USB-C 安装架跨在 PCB 上用于垂直应用，从而避免需要热空气。

[鉴于目前的芯片短缺](https://hackaday.com/2021/01/18/pandemic-chip-shortages-are-shutting-down-automotive-production/),【dojoe】表示，最大的问题可能实际上是如何获得 Twonkie 核心的 STM32F072CB 微控制器。为此，该板支持 TQFP44 和 QFN44 尺寸，您甚至可以使用 STM32F072C8，但会牺牲一些功能。运气好的话，希望你能在零件箱里找到一个能用的芯片。