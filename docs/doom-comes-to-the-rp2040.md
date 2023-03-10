# 末日降临 RP2040

> 原文：<https://hackaday.com/2022/03/15/doom-comes-to-the-rp2040/>

到了成为一个笑话的程度，似乎 *DOOM* 现在已经适应了在任何事情上运行。因此，很自然地，我们会[看到它被【格雷厄姆·桑德森】](https://kilograham.github.io/rp2040-doom/)移植到 RP2040，这是一个驱动树莓 Pi Pico 的小芯片。

你可能会想，这个港口有什么不同？Hackaday 上已经有 55 篇关于*毁灭*的文章，显示它运行在从[网络复选框](https://hackaday.com/2021/10/18/play-doom-using-web-browser-checkboxes-finally/)到[桌面手机](https://hackaday.com/2021/08/13/doom-on-a-desk-phone-is-just-the-tip-of-the-iceburg/)的所有东西上。RP2040 有 256 K 的内存，两个时钟不错的处理器内核，和 2 MB 的闪存，所以它不是运行它的最受限制的平台。但是[格雷厄姆]也设定了一些非常崇高的目标:所有九个级别都必须是可玩的，忠实的图形和音乐，多人游戏，并且它将直接输出到 VGA。它应该像原来一样播放。 *DOOM* 有一个演示，存储为输入事件序列。他们形成了优秀的回归测试，就好像角色卡住了或者没能坚持到最后；那你按照原码就不准确了。

一开始就有两个大问题。首先，单个级别大于 RP2040 的 2 MB 存储。为了驱动 320×200 的显示器，你要么需要花费大量的 CPU 预算来运行光束，要么需要分配大量的 RAM 给帧缓冲区，这使得级别解压缩更加困难。

默认的压缩方案不能满足它，因为它需要高压缩比和随机访问，因为解压缩到 RAM 不是一个选项。然而，仔细优化和压缩不同的数据结构会产生很好的结果。保存游戏文件给予了类似的处理，以确保它们适合所有级别(34k)后剩余的闪存。

结果很奇妙，支持*末日*、*终极末日*、*末日 II* 。这篇文章比我们在这里所能描述的要详细得多；享受阅读。如果你决定独自去地狱深处一日游，一定要在评论中告诉我们。

 [https://www.youtube.com/embed/eDVazQVycP4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eDVazQVycP4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢 [Hackaday Discord 服务器](https://discord.gg/NkbHrAW7NG)上的【Xark】提供的提示。