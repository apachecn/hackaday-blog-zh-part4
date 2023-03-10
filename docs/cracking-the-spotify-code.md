# 破解 Spotify 代码

> 原文：<https://hackaday.com/2021/12/07/cracking-the-spotify-code/>

如果你使用过 Spotify，你可能会注意到它可以生成一个方便的小代码，看起来像一系列不同高度的条形。如果你像[彼得·布恩]一样，这样的编码会激起你的好奇心，[你可能会着手弄清楚它们是如何工作的](https://boonepeter.github.io/posts/spotify-codes-part-2/)。

Spotify 提供了一张小图片，扫描后，几乎可以打开任何可以用 Spotify 搜索的内容。几行以 Spotify 标志为中心，有八种不同的高度，以八进制存储信息。许多视觉编码方案对某种 URI ( [统一资源标识符](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier))进行编码，该编码在解码时为特定歌曲、专辑或艺术家提供唯一标识符。由于 Spotify 上的许多 URIs 都很长(一个例子是 218 位的`spotify :show:3NRV0mhZa8xeRT0EyLPaIp`),需要某种机制将 URIs 压缩到更易于管理的程度。输入媒体引用，这是一个编码特定 URI 的短序列，通常小于 40 位。该引用只是在 Spotify 维护的数据库中进行查找，因此需要网络连接来解决。从媒体引用到条形中的值的实际编码方案相当复杂，包括 CRC、卷积和穿孔。CRC 允许程序检查解码是否正确，卷积使程序在有少量读取错误的同时仍有准确的结果。删截只是删除比特以减少编码的数字，依靠卷积来填补漏洞。

[Peter]在他的文章中解释了这一切，很有帮助，也很容易理解。Spotify 代码的创建者在评论中停下来提供了一些有价值的指示，包括指出还有第二种模式，其中行不居中，允许它存储双倍的比特。[Peter]在 Github 上有一个 [python 包，里面有你开始解码](https://github.com/boonepeter/boonepeter.github.io-code/tree/main/spotify-codes-part-2)所需的所有代码。也许你可以在你的定制 Spotify 播放迷你电脑的[中加入一个 Spotify 代码扫描器。](https://hackaday.com/2021/09/22/building-a-custom-linux-single-board-computer-just-to-play-spotify/)