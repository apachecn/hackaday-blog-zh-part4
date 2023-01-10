# 用固定电池骗过无人机

> 原文：<https://hackaday.com/2023/01/03/fool-a-drone-with-a-fixed-battery/>

锂离子和锂聚合物可充电电池给了我们以前不可能的电子功率和小型化的高度，但它们也带来了负面影响。当电池组必须包含用于平衡电池的电子设备时，制造商很容易增加额外的功能，例如锁定电池。修个电池，换个电池，或者用第三方电池，都不行。[Zolly]用一个 DJI Mavic Mini pack，[和我们分享一个绕过它的方法](https://www.youtube.com/watch?v=lnZyM3plN9Y)。

狼群通过一条串行线路与多转子对话，黑客会在适当的时候中断这条线路，阻止它告诉它的主人有问题。这是一个好的开始——但我们不禁对剩下的工作有些疑虑。在我们看来，断开两个电池之间的平衡线并用电阻分压器愚弄电池管理系统(BMS)就像用一根电线绕过保护 MOSFETs 一样，是一种灾难。它可能会工作，理论上电池可以用外部平衡充电器安全充电，但我们不确定我们是否愿意在商店里有一个这样修改的包。

这确实提醒我们，BMS 董事会有时会令人愤怒地将所有者拒之门外。我们曾经遇到过这种情况，第二代 iBook 电池在 BMS 复位后复活了，但这仍然不是一件不小心的事情。阅读我们的[电池组和 BMS 板指南](https://hackaday.com/2022/02/16/when-battery-rebuilds-go-wrong-understanding-bmss-spot-welders-and-safety/)了解更多信息。

 [https://www.youtube.com/embed/lnZyM3plN9Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lnZyM3plN9Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

