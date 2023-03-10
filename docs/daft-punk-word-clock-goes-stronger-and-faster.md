# 蠢朋克字钟走得更快更强

> 原文：<https://hackaday.com/2022/03/08/daft-punk-word-clock-goes-stronger-and-faster/>

你会把不显示时间的单词钟叫做什么？单词时钟的概念是所有需要使用的单词都已经存在，然后只需选择。[Ben Combee]意识到只有 18 个独特的词组成这首歌“更难更快更好更强”，手头上有一个来自 Supercon 2021 的额外 PyBadge，似乎很明显可以制作一个各种各样的音乐单词钟。

PyBadge 是一个基于 120 MHz ATSAMD51 的电路板，带有一个屏幕、按钮和一个他 3d 打印的外壳。为了获得合理的音质，同时仍然适合设备上的 2MB 闪存，选择了 MP3 压缩。由于只有一个扬声器，它被混合成单声道和较低的比特率，大小只有 880KB。mp3 由 circuitpython 中的 audiomp3 模块处理，音量被发送到五个新像素以充当 VU。获得正确的时间是最困难的部分，因为歌词需要被分离出来，并计算出时间。使用 Audacity 的标签跟踪特性，他在跟踪中标记了所有的单词，并可以将其导出为一种格式，这种格式可以转化为 python 友好的格式。

随着文件的播放，音乐和文本提示变得不同步成为一个更大的问题。增加 MP3 缓冲区有所帮助，但真正的技巧是偷看音乐解码器内部，并计算出有多少样本已被解码，并基于此提示单词，而不是时间，因为它不准确。所有的代码和文件[都在他的 Hackaday.io 页面](https://hackaday.io/project/183342-daft-punk-word-clock)上，如果你觉得有必要自己制作的话。如果你坚持蠢朋克，让 T2 在摇滚的时候准备好头盔。尽管基于这个[对流行歌曲](https://pudding.cool/2017/05/song-repetition/)可压缩性的总结，还是有一些其他歌曲有足够少的独特单词，它们也可以得到单词时钟的待遇。休息后的视频。

 [https://www.youtube.com/embed/fK78fMK-QzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fK78fMK-QzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

