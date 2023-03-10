# TEGA:打字稿嵌入式游戏机(宏)汇编程序

> 原文：<https://hackaday.com/2022/12/01/tega-typescript-embedded-game-boy-macro-assembler/>

弗朗西斯·斯托克斯(Francis Stokes)对最初的游戏男孩有着真正的爱，这表明拥有这台机器推动他走上了我们许多人都会认识的特定道路。从硬件角度来看，开发 Game Boy 游戏并不特别困难，因为你可以很容易地买到带有 SD 卡插槽的特殊卡带，允许自定义代码。【弗朗西斯】产生了通过制作一个打字稿硬件抽象库[【TEGA】(或者打字稿嵌入式 Game Boy 宏汇编器)](https://github.com/francisrstokes/tega) 来轻松进行软件开发的想法。这提供了一个安全的环境来玩代码，然后在部署到实际的硬件上之前，代码可以在模拟器中运行，如 [BGB](https://bgb.bircd.org/) 。

下面嵌入的视频——我们现在警告你这是一个很长的视频——对[Francis]如何利用 typescript 创建大量优秀功能来生成安全代码进行了广泛的论证和技术解释，同时处理了许多 Game Boy 的架构限制，以及支持它的夏普 SM83 处理器的怪异之处。我们特别喜欢对动态资产压缩的内置支持，因为每个字节在微薄的 32 Kb 系统中都很重要，不用一直考虑它是件好事！在讨论了 TEGA、游戏男孩硬件、试玩游戏 *的来龙去脉、方块跳跃* 以及如何与 BGB 一起调试之后，我们非常有信心，你们中的许多人将在未来开发出一款游戏男孩应用程序！

顺便说一句，我们也偶然发现了芬兰程序员和游戏男孩 superfan [Joonas Javanainen] 提供的 新硬件指南 [，这将有助于构建[Francis]正在谈论的一些主题。](https://gekkio.fi/files/gb-docs/gbctr.pdf)

你可能还记得不久前，同一个作者使用用打字稿 编写的代码瞄准了 [RISC-V。毕竟，当你对一个工具得心应手的时候，你可以让它做任何事情。](https://hackaday.com/2021/10/14/risc-v-in-typescript/)

 [https://www.youtube.com/embed/TIlx5nBnx-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TIlx5nBnx-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

