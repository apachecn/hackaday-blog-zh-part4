# 看看强大的软盘驱动器 3.0

> 原文：<https://hackaday.com/2022/06/14/behold-the-mighty-floppotron-3-0/>

如果有人最近一直在努力获得一个 3.5 英寸的软盘驱动器，我们认为我们已经找到了一个线索，看看[帕韦·zadrożniak.]的强大的软盘驱动器 3.0floppotron 3.0 MIDI 合成器拥有一个完全疯狂的 512 个软盘驱动器、4 个平板扫描仪和 16 个不同大小的硬盘，可能是迄今为止最大的这种复古硬件合成器。由于该系统的每个部分都是基于电机的，所以没有人会惊讶为演出供电是一项艰巨的任务，需要近 20 个开关模式 PSU 模块来满足需求，平均功率为 300W，但额定峰值为 1.2kW！

基于 nRF52xx 系列 MCU 的全定制 MIDI 转 RS485 网关处理与![](img/0816c62e84f41b0034d53a2621128681.png)仪器控制器集合的通信。这些控制器足够通用，可以接受 RS485 输入并控制一个专用驱动器，用于一组软盘驱动器(最多 192 个)、一组硬盘驱动器或少量扫描仪。软盘驱动器的分组方式非常简洁。该软件对每个音符使用整列，而不是使用每个驱动器来产生特定的音调。随着时间的推移，通过改变同时移动的驱动器数量，音量会发生变化，从而模拟音符包络并产生更丰富的声音。多列并行驱动赋予系统 16 个音符的复调。软盘覆盖低音，四个平板扫描仪覆盖高音。MIDI 鼓的声音被映射到硬盘上，以一种打击乐的方式运行，不同的外壳形状产生独特的声音。甚至固件都可以通过 MIDI 更新！因此，休息之后，请观看演示视频，欣赏由捷克作曲家朱利叶斯·富契克创作的非常熟悉的《角斗士进行曲》。

如果你认为这看起来很熟悉，你没有错，我们已经涵盖了之前的[更早的软盘驱动器，但我们估计还没有人试图用](https://hackaday.com/2016/07/13/nirvana-like-youve-never-heard-them-before/)[叶旧的八英寸](https://hackaday.com/2021/11/10/8floppy-on-your-pc/)驱动器做到这一点！

 [https://www.youtube.com/embed/kCCXRerqaJI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kCCXRerqaJI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[electronoob]和[Ruhan van der Berg]的提示！