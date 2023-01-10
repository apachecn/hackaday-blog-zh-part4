# 华丽的 Perfboard 构建使 1 位控制器恢复工作

> 原文：<https://hackaday.com/2020/11/06/gorgeous-perfboard-build-puts-1-bit-controller-back-to-work/>

如今，八位计算机风靡一时，人们争先恐后地用 6502 或 Z80 这样的芯片制造计算机，甚至用一批 TTL 逻辑芯片再造这些芯片。虽然我们非常尊重和觊觎这些构建，但 8 位计算机并不是唯一的游戏。也就是说，我们展示了这款可爱的单板电脑，配备了 1 位 CPU。

这台被创造者[西蒙·博克]戏称为“世界上最弱的计算机”的机器是基于摩托罗拉 MC14500B 的，这是一款 20 世纪 70 年代针对工业控制市场的芯片。在那里，芯片有限的指令集和狭窄的总线宽度不像在通用计算机中那样受到限制。事实上，由于芯片需要一个外部程序计数器，它提供了很大程度的设计灵活性。[Simon]选择了一个 4 位地址空间，但通过一点小技巧，他能够以 DIP 开关的形式获得 8 位输入和 8 位输出 led。过去让灯闪烁不是很好，但它在没有 Arduino 的情况下做到了这一点——尽管它确实有几个 555。

[Simon]的构建目标只是用一个不寻常的芯片来构建 cool，我们认为他成功了。事实上，我们不记得见过更整洁的 perfboard 构建——它几乎达到了电路雕塑的水平。我们特别喜欢混合焊接和绕线结构。在之前，我们已经看到过基于这个芯片的[构建，但从来没有一个如此整洁和吸引人。](https://hackaday.com/2020/02/01/what-everyone-else-did-with-eight-bits-the-germans-did-with-only-one/)

[通过[遥控/电子](https://www.reddit.com/r/electronics/comments/jm24h2/i_built_a_1bit_cpu_around_the_mc14500b_industrial)