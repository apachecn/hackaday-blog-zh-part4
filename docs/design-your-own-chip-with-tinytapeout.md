# 用 TinyTapeout 设计自己的芯片

> 原文：<https://hackaday.com/2022/10/23/design-your-own-chip-with-tinytapeout/>

当黑客们发现并开发出低价订购 PCB 的方法时，它彻底改变了我们的创作方式。无障碍 3D 打印给我们带来了全新的创造空间。[Matt Venn]是站在黑客前沿设计我们自己的芯片的人之一，多年来我们已经报道了他的大量研究。他让黑客社区参与进来的最新努力， [TinyTapeout，](https://tinytapeout.com/)让芯片设计对新来者变得触手可及——门槛低得就像在网页浏览器页面上排列逻辑门一样。

![Six chip shots shown, with various densities of gates being used - some use a little, and some use a the entire area given.](img/fbc42fe98f981b61bd8e35131c026007.png)

Just six of the designs submitted, with varying complexity

为此，[Matt]与 Wokwi fame 的[Uri Shaked]、[Sylvain "tnt" Munaut]、[jix]和其他一些人一起工作。他们一起创建了所有必要的工具，最重要的是，在 Wokwi 中基于逻辑门的[设计被编译成一个模块，准备投入芯片，甚至模拟和编译时验证常见错误。因此，设计过程非常简单，一个 9 岁的孩子](https://wokwi.com/projects/339800239192932947)就能[做到。如果你愿意，你也可以提交你的 Verilog！](https://twitter.com/matthewvenn/status/1566377267298697221)

TinyTapeout 的第一轮截止日期是九月初和[汇集了 152 个参赛作品](https://tinytapeout.com/tt01/)——正好赶上 Efabless shuttle 提交。所有这些设计都被放在一个单独的芯片上，这个芯片将被批量制造、测试、焊接到分线点上，然后邮寄给每个参与者。通过这种方式，每个人都将获得每个人的设计，但由于片内多路复用硬件，他们能够使用分线开关在设计之间切换。

休息后更多…

约束很简单。你得到 8 个数字输入，8 个数字输出，有 200 个门供你使用。你能用这个造什么？首先，一个 [BCD 到 7 段解码器、](https://twitter.com/jg_lim/status/1575817966805188608)[UART 发送器、](https://twitter.com/maehw/status/1565654207444783104)甚至是一个[全 4 位 CPU](https://github.com/tommythorn/tinytapeout-4-bit-cpu)——或者，一个狼、羊和卷心菜游戏！在第一轮提交结束后，[Matt]要求人们收集关于他们设计的信息——这里有[一个 PDF 数据表](https://tinytapeout.com/tt01.pdf)，有 30 多种不同的设计供您惊叹，从 Hello World ones 到 CPU，各种具有实用或教育目的的电路。

此刻，[Matt]已经在计划下一次 TinyTapeout 跑了。如果你有一个项目想法要求进入冷酷的逻辑门，[注册邮件列表](https://tinytapeout.com/tt02/)，你就不会错过下一个 TinyTapeout 截止日期的消息。 [Wokwi 模板](https://wokwi.com/projects/339800239192932947)已经为你的实验目的开放，剩下的就是打开提交表单。如果你有任何问题，[常见问题解答](https://tinytapeout.com/faq/)很有帮助！

当然，这样的项目不会凭空出现——几年来，[Matt]一直在给我们带来如何进入芯片设计的黑客教学。我们在 2020 年举办了他的[零到 ASIC 研讨会，](https://hackaday.com/2020/12/29/remoticon-video-from-zero-to-asic-how-to-design-in-silicon/)在 Remoticon 2021 举办了 [OpenMPW 进展故事](https://hackaday.com/2022/02/17/remoticon-2021-matt-venn-helps-you-make-asics/)，就在今年，[举办了关于开源 ASIC 的黑客聊天。](https://hackaday.com/2022/03/18/the-open-source-asics-hack-chat-redefines-possible/) TinyTapeout 让我们想起了【OSHPark 如何成立的故事——一群人凑在一起订购他们的 PCB，就像那时一样，我们预见到普通黑客的工具包中会增加一些有趣的东西。

 [https://www.youtube.com/embed/uDlOeJAUmzs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uDlOeJAUmzs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

