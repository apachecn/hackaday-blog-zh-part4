# 软盘上的 45 分钟播客

> 原文：<https://hackaday.com/2020/08/09/45-minute-podcast-served-up-on-a-floppy-disk/>

在世纪之交，像 iPod 这样的便携式媒体播放器引领了播客的发展。该格式通常由类似于基于谈话的广播的内容组成，通常在 AAC、M4A 和 MP3 等现代编解码器中提供。然而，[Sean Haas]认为这些都太厚了，想看看是否有可能在软盘上提供类似的内容。结果是可预见的，但令人印象深刻。

[Sean]的目标是尝试将大约 45 分钟的音频存储到 1.44 MB 的软盘上。为了实现这一目标，他四处寻找适合这项任务的编解码器。最终的选择是自适应多速率，或 AMR。它通常用于对 GSM 电话的音频进行编码，也可用于创建压缩音频文件。

最初的尝试不够好，所以[Sean]引入了 FFMPEG 的预处理步骤，将音频速度提高了 1.2 倍。然后，它通过 SoX 并以大约 5 kbit/s 的速度在 AMR 中编码。这使得一个 45 分钟长的 72MB 的 MP3 文件被压缩到仅 1.2 MB，因此能够放入软盘。音频质量是可预见的差，因为你可以听到下面的嵌入剪辑，但绝对可以理解。如果你认真做这件事，你可能会想跳过任何音乐片段。

[https://open.spotify.com/embed-podcast/episode/2Hysj8riEwr2lxVPW7DtjK](https://open.spotify.com/embed-podcast/episode/2Hysj8riEwr2lxVPW7DtjK)

[Sean]更进一步，转换了他的整个旧目录，并创建了一个 RSS 提要。这然后被提交到通常的播客目录，如苹果播客，谷歌播客等。虽然大多数人拒绝提交，因为他们缺乏对 AMR 文件的支持，但不知何故 Spotify 对内容没有问题。【Sean】怀疑某处一定在进行某种转换，因为浏览器通常没有内置 AMR 播放器。

这是一个有趣的项目，我们几乎感到失望的是，在软盘交易和 BBSes 时代，没有人尝试这样做。如果你对压缩音频标准的历史以及它们如何改变世界感兴趣，[我们很乐意满足](https://hackaday.com/2020/07/27/mp3-is-25-years-old/)。

 [https://www.youtube.com/embed/E4ur2yaFzgE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E4ur2yaFzgE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

