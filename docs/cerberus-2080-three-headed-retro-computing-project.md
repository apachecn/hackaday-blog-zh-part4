# Cerberus 2080——三头复古计算项目

> 原文：<https://hackaday.com/2021/06/08/cerberus-2080-three-headed-retro-computing-project/>

七个月来，[the byteatic]的[贝尔纳多·卡斯特鲁普]一直在实现他儿时的梦想，那就是建造自己的电脑。正是这个梦想让他在 17 岁时进入了计算机设计领域。在这个行业干了三十年后，他终于有时间设计他小时候梦想的电脑了。他的要求是雄心勃勃的:完全开放的设计，门级细节，便于黑客攻击的通孔或 PLCC，具有现有工具链的成熟处理器，用于 CPLDs 的低成本开发工具，无 FPGA，标准 ITX 案例兼容，等等。他很合理地决定使用更现代的电子设备来做视频(VGA)、键盘(PS/2)和程序存储(闪存盘)。与此同时，他选择在主板上放置三个处理器，而不是一个:

*   Zilog Z84C0010 (Z80)
*   WDC W65C0256 (6502)
*   AVR ATMEGA328 (RISC 控制器)

当提出概念和要求时，[Bernardo]脑海中有一个虚构的替代历史，其中有 ZX80、PET/CBM 或 TRS-80 的后续产品，它们是原系统的扩展。但他也想要一个简洁的设计，没有削减成本的噱头，以便让学习者更容易专注于计算本身——正如他所描述的那样，这是一种说教式的架构。转动曲柄七个月，我们就有了地狱犬 2080。【Bernardo】已经把[的设计放到了 GitHub](https://github.com/TheByteAttic/CERBERUS2080) 上，把整个过程做了一个视频系列出来，其中介绍视频在休息下面。甚至还有一个由复古黑客安迪·图恩开发的[在线模拟器](https://feertech.com/legion/cerberus.html)。

我们在 2014 年写了关于基于 6502 的 ERIC-1 项目[，它与 ATMEGA 模拟 ROM 共享总线。【2019 年的 Minty Z80 项目](http://petenpaja.blogspot.com/2014/11/eric-1-homebrew-computer-part-1.html)也采用了类似的技术。感谢[弗雷德里克]给我们发来的提示。

 [https://www.youtube.com/embed/1ASspLiE39g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1ASspLiE39g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

