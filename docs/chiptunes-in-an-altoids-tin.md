# Altoids 罐中的薯片

> 原文：<https://hackaday.com/2018/10/27/chiptunes-in-an-altoids-tin/>

对于[Dejan]参加今年 Hackaday 奖的乐器挑战，他利用了多年来为大众带来哔哔声和哔哔声而做的一些伟大工作。他正在制作一个鼓机、一个低音合成器和一个适合你口袋的自动琶音器，它的外形很方便，可以放在一个 Altoids 罐里。[是 FATCAT Altoids Tin Mod 追踪器](https://hackaday.io/project/161396-fatcat-altoids-tin-mod-tracker)。

这是一个简单的构建，可以放在一个 Altoids 罐中，所以这里没有太多的硬件。有一个电池，有一个升压电路，还有一个单独的芯片，一个 ATtiny84。这个微小的微控制器是盒子的心脏，能够提供鼓轨道，带有脚鼓、小军鼓和一个封闭和开放的高帽。有一个简单的方波和滑音的低音，和一个 arp 轨道，可以用作引导或琶音和弦。所有这些都是用 C 语言编写的，直接上传到芯片上。

ATtiny 系列微控制器因其产生方波哔哔声和滴声的各种方式和方法而广受欢迎。我们已经看到它们变成了适合 MIDI 插孔的 MIDI 合成器，我们也看到了在 32 字节的 RAM 中可以容纳多少 chip tune goodness(T2)。康奈尔大学甚至发生了一起里克罗尔破坏公物的口角，起因是一个硬币电池投掷器建在一个 85 号的 T5 上。在我们的书里，任何能让更多人接触到更多 ATtiny chiptunes 的东西都是伟大的，而这个 Altoids tin synth 正是我们想要的。

你可以看看下面这只肥猫的演示。

 [https://www.youtube.com/embed/Ccxs5wTrU1g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ccxs5wTrU1g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)