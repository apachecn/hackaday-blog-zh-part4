# Aqua PCB 是 Mattel Aquarius 的一大升级

> 原文：<https://hackaday.com/2022/10/15/aqua-pcb-is-a-big-upgrade-for-the-mattel-aquarius/>

如果你不在 80 年代，或者你碰巧眨眼，你可能错过了美泰水瓶电脑。尼克·比尔德对这台机器情有独钟，他制造了 [Aqua cartridge](https://hackaday.io/project/187458-aqua) 来使水瓶号成为一台更有用的机器。

最初只配备了 4 KB 的内存和一个小的橡胶键盘，所以 Aquarius 在市场上只持续了五个月也就不足为奇了。[Nick]考虑到设备上的扩展端口数量较少，决定使用墨盒插槽来增强这台小机器的规格。增加 32 KB 的内存无疑会提高它的性能，他还设计了一个名为 Aqua Write 的 SD 卡接口，可以连接到 Aqua cartridge，以便轻松地从更现代的机器上传输文件。

Aqua Write 使用 Arduino Mega 2560 来处理 SD 卡和系统内存之间的移动数据。这有点复杂，因为“PLA 位于 Z80 和数据总线之间，用软件锁代码(启动时初始化为随机值)对数据进行异或运算。”[ Nick 通过运行一个小程序在启动后将锁码覆盖为零来解决这个问题。

从逆向计算机上获取数据肯定是一个挑战。如果你试图从另一台旧机器上获取文件，试试这个简单的通用调制解调器或者考虑用树莓 Pi 作为虚拟软盘驱动器的 T2。