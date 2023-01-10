# 让微通道总线计算机发出声霸声

> 原文：<https://hackaday.com/2020/12/01/giving-micro-channel-bus-computers-a-sound-blaster-bark/>

今天可能没有多少人记得“微通道架构”是什么，尽管它的首字母缩写“MCA”可能听起来耳熟。由 IBM 创建，用来取代 ISA(工业标准体系结构),并可能收回一些甜蜜的许可费，但它并不像 IBM 希望的那样成功。历史告诉我们，PCI 最终在 IBM 的所有系统中取代了 MCA。使用 MCA 的 IBM PS/2 系统没有错过经典的 20 世纪 90 年代卡，例如最初的声霸卡，但是今天 MCA 版本的声霸卡不可否认地相当…罕见，更不用说昂贵了。

但是，现在不再是了:在最后一批 PS/2 用户离开几十年后，[Tube Time]自豪地推出了 [Snark Barker MCA](https://github.com/schlae/snark-barker-mca) 。这是一个完全兼容 Sound Blaster 的声卡。它支持即兴合成，数字声音回放和录音，以及操纵杆输入和 MIDI。它基于 Xilinx XC9572XL CPLD，并具有看起来像全长 MCA 卡的功能，它会让原始的声霸卡感到自豪。

GitHub 库不仅包含 CPLD 的原理图、BOM 和基于 Verilog 的 HDL，还包含大量关于汇编和编程的文档。另外，还有一个故障排除部分，介绍了跨系统草率实现 MCA 带来的一些乐趣。绝对值得一读。

如果有人决定构建这个项目并在他们的 IBM PS/2 系统中使用它，我们很乐意听到这个消息。

当然，如果你需要的只是一个普通的 PCI 声霸克隆版本，那么最初的 Snark Barker 是你的不二之选。

(谢谢，戴瑞)