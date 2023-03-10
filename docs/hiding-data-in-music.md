# 在音乐中隐藏数据可能是摆脱咖啡店 WiFi 密码的关键

> 原文：<https://hackaday.com/2019/07/15/hiding-data-in-music/>

苏黎世联邦理工学院(ETH Zurich)的两名博士生想出了一个有趣的方法来将信息嵌入音乐中，这一举动肯定会让音响发烧友们退回到他们原始的声音洞穴中。这听起来很疯狂，因为他们将数据牢牢隐藏在 9.8 kHz 到 10 kHz 的可听频谱中。问题是，*听起来真的很疯狂吗？不是我们的耳朵，回放仍然令人惊讶地好。*

你可以在 ETH 的网站上听一段有数据和没有数据的剪辑，自己去看。举个简单的例子，这是 12 秒钟的音频，展示了同一个片段的两个版本。第一个片段没有数据，第二个片段有编码数据。

<https://hackaday.com/wp-content/uploads/2019/07/ZTH-no-Filter.mp3?_=1>

[https://hackaday.com/wp-content/uploads/2019/07/ZTH-no-Filter.mp3](https://hackaday.com/wp-content/uploads/2019/07/ZTH-no-Filter.mp3)

你可能会说服自己这是有区别的，但这种区别可以忽略不计。即使我们使用 8 kHz -10 kHz 范围内的 janky 带通滤波器来突出差异，也不容易区分您听到的内容:

<https://hackaday.com/wp-content/uploads/2019/07/ZTH-with-8k-10k-filter.wav?_=2>

[https://hackaday.com/wp-content/uploads/2019/07/ZTH-with-8k-10k-filter.wav](https://hackaday.com/wp-content/uploads/2019/07/ZTH-with-8k-10k-filter.wav)

在表演现场音乐和涉足录音棚多年后，我会把数据编码剪辑描述为有微弱的反馈或奇怪的混响效果。然而，你不会在杂货店扬声器播放的音轨中注意到这一点。

## 为什么要使用音频？

你究竟为什么要用音频来传递信息呢？简单的答案是到处都有声音发射器和接收器。特别是手机。根据研究人员的说法，这比超声波效果更好，因为手机麦克风在高频下灵敏度低，衰减速度比音频快。

通过将数据编码到音乐的听觉范围内，咖啡店可以在 Sia-heavy 播放列表中广播它们的 WiFi 密码。(为什么总是 Sia？)手机可以检测密码并自动连接。

## 为什么听起来不错:OFDM 和掩蔽频率

 [![Masking data in harmonic frequences](img/2214fa8a282ca7c4e1a2e55e00d9ee51.png "Masking data in harmonic frequences")](https://hackaday.com/2019/07/15/hiding-data-in-music/masking-data-in-harmonic-frequences/)  [![Processing steps used](img/8d765b53f7fa9046f33bfc430753a740.png "Encoding Process")](https://hackaday.com/2019/07/15/hiding-data-in-music/encoding-process/) Processing steps used

[原始论文](https://tik-old.ee.ethz.ch/file/8a61c16532c1d4f9021d3aaf06f4f381/imperceptible_audio_communication.pdf)更详细，但系统不会破坏音乐，因为它使用音乐来掩盖数据。它检测轨道中最强的频率，并在频率的谐波周围嵌入数据。这样，编码数据听起来就像是音乐的一部分。

当然，它不只是在一个频率上编码数据。它采用[正交频分复用](https://en.wikipedia.org/wiki/Orthogonal_frequency-division_multiplexing) (OFDM)。OFDM 本质上是将传输分散在多个载波频率上，以降低单个频率的功率。它用于 4G 和 802.11a 无线局域网等技术中。OFDM 允许系统在最小化特定音调的幅度的同时，在一个频带中推进更多的功率。

不出所料，数据传输速率远不及光纤速度。使用低频载波有它的缺点。研究人员能够达到 300-400 比特/秒(是的，比特不是字节)。不过，传输距离和精确度相当不错，在 24 米处，误码率不到 10%。BER 和数据速率因歌曲而异，皇后乐队和街头霸王乐队乐队首当其冲。

在现实世界中，他们期望大约 200 比特/秒，这足以每秒发送大约 25 个单词。这足以快速传输文本信息或简单的数据流，但你不会想用这种数据链接浏览潮湿的迷因。

感谢【Qes】的[提示](https://newatlas.com/phone-data-transmitted-through-music/60514/)！