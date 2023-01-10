# 最终幻想 Exploit 教授 32 位整数数学

> 原文：<https://hackaday.com/2018/09/19/final-fantasy-exploit-teaches-32-bit-integer-math/>

除了明显的怀旧之外，旧视频游戏的一个有趣之处是，一些更受欢迎的游戏多年来一直被拆开和修补，导致游戏中出现了许多新的“开发”。这通常会发现一些隐藏的宝石，这些宝石在游戏全盛时期可能没有任何知识，比如在《最终幻想 7》中发现的这种奇怪的编码，它说明了 32 位处理器如何做数学。

最初的 PlayStation 使用 32 位 RISC 处理器，但最高有效位可用于[整数签名](https://en.wikipedia.org/wiki/Signed_number_representations)。这意味着，如果您有一个值为 2，147，483，647(二进制为 011111111111111111111111111)的整数，并且您添加了一个，则该值会突然变为负 2147483648，因为最高有效位也是整数符号的指示符。在这种情况下，整数被称为“溢出”。在《最终幻想 7》中，如果你能以某种方式让一个角色一击造成 262，144 点伤害(远低于 20 亿，因为游戏计算伤害的方式)，这个游戏就有点崩溃了。

[4-8Productions]不得不做大量的工作来展示这个小故障如何在游戏中被利用。通常这个游戏中的伤害限制在 9999，但是在某些配置下(当然是通过使用 FF7 可用的其他漏洞和工具如 savegame 编辑器获得的)，两个角色可以造成比这个临界值更大的伤害，这暴露了 32 位处理器的弱点。

尽管整数签名对我们大多数人来说是一个非常基本的概念，但这个视频绝对值得一看，尤其是如果你是这个经典游戏的粉丝。当然，《最终幻想 7》并不是唯一一部被利用和逆向工程到极致的经典。你现在也可以使用超级马里奥世界关卡[来实现计算器](https://hackaday.com/2016/02/10/calculator-built-in-super-mario-level-mamma-mia/)。

 [https://www.youtube.com/embed/cFYdr4X2Nqo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cFYdr4X2Nqo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

