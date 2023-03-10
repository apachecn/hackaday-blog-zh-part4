# Shell 脚本合成器击败您的 SoX

> 原文：<https://hackaday.com/2018/08/02/shell-script-synthesizer-knocks-your-sox-off/>

Sound eXchange，或 SoX,“音频操作的瑞士军刀”自 Linux 内核以来就一直存在，如果您不熟悉它，它是一个用于播放、录制、编辑、生成和处理音频文件的命令行工具。[porkostomus]对生成部分特别感兴趣，并编写了一个小小的 shell 脚本[，它利用 SoX 的内置合成器来创作 8 位风格的音乐](https://github.com/porkostomus/mecca)。

该脚本带有一个简单而直接的用户界面，可以将主音和低音部分录制到一个文本文件中，并在以后播放它们。目前支持从 C2 到 C5 的音符，并映射到两行钢琴布局中的键盘。输出文件格式本身只是一个纯文本列表，列出了演奏的音符、波形和音符长度。这让您可以轻松地编辑乐曲，甚至从替代来源(例如 MIDI)生成乐曲。还要注意，这里不需要初始音频文件，SoX 会根据需要生成它们。

诚然，命令行界面可能不是创作音乐最方便的方式，但无论如何，它是一种方式——这是[porkostomus]在这里的主要任务。此外，SoX 很有趣，而且用途广泛，[你甚至可以将它的音频效果应用到图像上](https://hackaday.com/2017/04/16/mangling-images-with-audio-effects/)，或者[用它解码从直升机](https://hackaday.com/2014/02/02/decoding-news-helicopter-signals-on-youtube/)发出的奇怪信号。