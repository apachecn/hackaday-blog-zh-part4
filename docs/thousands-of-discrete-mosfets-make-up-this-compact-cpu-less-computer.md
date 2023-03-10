# 数千个分立的金属氧化物半导体场效应晶体管组成了这台紧凑的无 CPU 计算机

> 原文：<https://hackaday.com/2021/05/19/thousands-of-discrete-mosfets-make-up-this-compact-cpu-less-computer/>

多久没有一台电脑可以夸耀它包含 2500 个晶体管了？据猜测，现在可能接近半个世纪了。因此，在一个每个芯片有几十亿个晶体管的世界里，一台 2500 个晶体管的计算机真的值得夸耀吗？是的。没错，就是。

这种无 CPU 的计算机被它的创造者[Dennis Kuschel]称为 TraNOR，是对他以前的[my NOR](https://hackaday.com/2020/11/23/a-cpu-less-computer-with-a-single-nor-gate-alu/)的详细阐述，这是另一种无 CPU 的机器，使用由分立晶体管制成的单个 NOR 门作为其算术逻辑单元(ALU)的核心。尽管架构简单，MyNOR 还是有相当不错的表现，甚至还玩了一个不错的俄罗斯方块游戏。另一方面，TraNOR 要复杂得多，主要是因为[Dennis]没有依赖 74HC 系列芯片，而是用分立的 MOSFETs 构建了机器上的每个栅极。四个堆叠的 PCB 上仅有的芯片是三个一组的存储芯片；我们不会因为他决定不建立记忆而责怪他——他可能很专注，但即使是艺术也有其局限性。TraNOR 确实是一件艺术品——下面的视频展示了漂亮的电路板布局，看似无穷无尽的 SMD 晶体管阵列排列整齐，焊接仔细。另外，使用[温特加坦的弹珠机旋律](https://hackaday.com/2016/03/03/incredible-marble-music-machine/)作为配乐也是加分的。

虽然我们很喜欢原版，但 TraNOR 确实很特别。它不仅漂亮，而且实用——它甚至可以向后兼容 MyNOR 的定制软件。向[Dennis]致敬，感谢他完成了另一个精彩的构建，并与我们分享了它。

 [https://www.youtube.com/embed/VgktjP_Fcy8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VgktjP_Fcy8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

