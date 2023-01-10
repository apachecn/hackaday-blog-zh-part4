# CortexProg 是一个真正的强制手段

> 原文：<https://hackaday.com/2018/07/17/cortexprog-is-a-real-arm-twister/>

我们的桌面上有一小盒微控制器程序。AVR，PIC，和 ARM，或者至少是 ARM 的 STMicro 版本。为什么？有些程序更快，有些调试更好，有些有更好的电缆，而其他的，嗯，我们只是对这些有点感情用事。不要妄加评论。

另一方面，德米特里·格林伯格正在寻找至尊魔戒。或者至少是 ARM 微控制器的[环。你看，虽然所有 ARM 芯片都有相同的内核，因此也有相同的 SWD 调试接口，但它们都以不同的方式写入闪存。因此，如果你使用不同芯片供应商的产品进行 ARM 开发，你需要一个装满程序员的盒子，或者购买一个昂贵的 J-Link。直到现在。](http://dmitry.gr/?r=05.Projects&proj=26.%20CortexProg)

[Dmitry]通过加载特定于闪存的代码部分作为插件来保持他的选择，这让程序员可以判断出它正在处理什么芯片，然后查找适当的块大小和闪存程序。一枚戒指。他还实现了一个快速的`printf`风格的调试辅助工具，他称之为“零线跟踪”,我们想知道更多。编程和调试在 Lua 中是可脚本化的，它可以基于读取芯片 id 进行批量编程。

你可以从 ATtiny85、两个二极管和两个限流电阻构建自己的 CortexProg:标准的 [V-USB](https://www.obdev.at/products/vusb/index.html) 设置。DIY 的缺点是什么？上传速度慢，但至少能让你继续。他还在此基础上开发了许多更好的版本。如果你感兴趣的话，硬件的第四个版本刚刚在 Kickstarter 上[上线。](https://www.kickstarter.com/projects/1182544591/cortexprog?token=b3f5f32c)

如果你只是使用一个供应商的芯片，或者不介意有一抽屉的程序员，你也可以看看[黑魔法探测器](https://hackaday.com/2016/12/02/black-magic-probe-the-best-arm-jtag-debugger/)。它在调试器中嵌入了一个 GDB 服务器，这既是一个很酷的技巧，也是你必须刷新程序员以使用不同供应商的芯片的原因。由于 BMP 固件是开放的，你可以自己制作一个牺牲性的 ST-Link 克隆，大约 4 美元。

另一方面，如果您想要一个跨芯片家族工作的、可脚本化的、可以批量上传的程序员，那么 CortexProg 看起来就像一个鱼饵预算有限的鱼子酱程序员。我们很快会尝试一个。

哦，如果你觉得[德米特里·格林伯格]听起来很熟悉，你可能会喜欢他的[甜蜜的梦幻 VRU 黑客](https://hackaday.com/2017/07/17/completely-owning-the-dreamcast-add-on-you-never-hadcompletely-owning-the-dreamcast-add-on-you-never-had/)，他的[对赛普拉斯的调查](https://hackaday.com/2017/03/04/reading-the-unreadable-srom-inside-the-psoc4/)，或者他的史诗般的[基于 AVR 的 Linux 机器](https://hackaday.com/2012/03/28/building-the-worst-linux-pc-ever/)。