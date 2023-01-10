# 一个简单而功能丰富的可编程 DC 加载器

> 原文：<https://hackaday.com/2020/02/28/a-simple-yet-feature-packed-programmable-dc-load/>

如果你渴望拥有一个充满高端设备的实验室，但你的预算却在抗议，那么滚动自己的测试设备可能是一个很好的选择。当然，并不是整个商店需要的所有东西都适合 DIY 版本，但是像这样的可编程 DC 负载对于大多数黑客来说肯定是可以实现的。

这个版本由[Scott M. Baker]提供给我们，他像往常一样做着记录一切顶级工作。下面有一个很长的视频，涵盖了从设计到测试的所有内容，而上面的链接是 events 的一个更简洁的版本。无论哪种方式，您都会对设计基础有一个很好的描述，它本质上是一个运算放大器，控制 MOSFET 的栅极与电流检测电阻上的电压成比例。最后一个电路添加了铃铛和哨子，主要是以三个 MOSFETS 和一个小 DAC 的形式来控制设定点。DAC 由 Raspberry Pi 驱动，该器件还支持 LCD 或 VFD 显示器、用于读取检测电阻两端电压的 ADC 以及用于远程控制负载的 web 接口。[Scott]的测试揭示了一些问题，比如运算放大器的失调电压导致的实际安培数读数的小差异。MOSFETs 在 100 W 的满载下也变得有点热；更大的散热器让他可以将负载推到 200 W 而不释放烟雾。

我们总是喜欢[贝克博士]的项目，尤其是他们对设计决策的洞察力。无论你是想为一台 40 年前的游戏主机升级控制器，还是想为一台 RC2014 的控制器配音，你都应该看看他的东西。

 [https://www.youtube.com/embed/CtzgRFZtyB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CtzgRFZtyB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

