# 幸运之轮在 NES 得到无限的困惑

> 原文：<https://hackaday.com/2018/12/02/wheel-of-fortune-gets-infinite-puzzles-on-nes/>

幸运之轮是一个电视游戏节目，诞生于遥远的 1975 年。像那个时代许多受欢迎的电视节目一样，它在各种平台上催生了一系列视频游戏。像许多黑客一样，[Chris]在他的 Raspberry Pi 上加载了复古的 NES 游戏，这时他意识到，由于盒式磁带格式的限制，他一遍又一遍地玩着同样的游戏。除了加载一个十六进制编辑器并开始工作之外，别无他法。

[Chris]最初的研究包括在十六进制编辑器中加载 ROM，并简单地搜索游戏中常见谜题的 ASCII 字符串。最初的结果是积极的，发现了一些明文碎片。最终，很明显谜题是以 ASCII 码存储的，但是为了标记换行和谜题结束，某些最高有效位被改变了。[Chris]命名为 wheelscii 格式，并开发了一个编码器，可以将新的谜题转换成相同的格式。

在进行了一些包括破坏谜题和测试各种边缘情况的初步实验后，[Chris]决定实施一个完整的修复。谜题来源于[幸运之轮谜题简编，](https://sites.google.com/site/wheeloffortunepuzzlecompendium/home/compendium)应该有足够的新鲜内容，除了最上瘾的观众。然后创建了一个脚本，在加载时将 1000 个新的谜题填充到 ROM 中，以最小化看到重复谜题的机会。

ROM 黑客总是很有趣，这是一个特别好的例子，说明如何用简单的工具对 30 年前的软件进行有趣的修改。再来一次，[看看这个让马里奥兄弟一起玩的游戏。](https://hackaday.com/2018/11/19/nes-hack-lets-the-mario-bros-play-together/)