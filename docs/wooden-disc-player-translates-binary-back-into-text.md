# 木制光盘播放器将二进制翻译成文本

> 原文：<https://hackaday.com/2020/09/18/wooden-disc-player-translates-binary-back-into-text/>

[![](img/efd8f2edb6afe3978145ba52cd004737.png)](https://hackaday.com/wp-content/uploads/2020/09/wooden-disk-player-matlab.png)

【jbumstead】用 MATLAB 将短信转换成二进制从磁盘中剪切出来。

【jbumstead】想要展示信息存储设备的想法，比如 LP、CD 和旧硬盘。他想出的东西直接位于艺术和技术的交汇点:[一台制造复杂的机器，可以播放美丽的拼贴木盘](https://www.instructables.com/id/Wooden-Disc-Player/)。很像激发木制磁盘播放器的媒体，它使用激光读取编码数据，在这种情况下，编码数据是像“不要惊慌”这样的简短文本。

这些片段以二进制存储，由一对激光和光电二极管读取，寻找光盘上的孔和非孔。该信息然后被发送到 Arduino Nano，Arduino Nano 将其翻译成英语，并在 LED 矩阵上滚动文本。更有趣的是，Nano 每次读取 1 时都会播放 MIDI 音符，你可以通过保护性的丙烯酸盾看到激光读取磁盘。

虽然最终的结果很棒，但是[jbumstead]在开发过程中遇到了很多问题，我们将在休息之后的构建视频中探讨这些问题。我们喜欢人们向我们指出他们的错误，因为这发生在我们每个人身上，我们不应该让它告诉我们停止黑客行为。

如果有人知道激光的方法，那就是[jbumstead]。我们喜欢在 Supercon 演奏他们的激光竖琴！

 [https://www.youtube.com/embed/RjRvGotzcRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RjRvGotzcRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通路〔t0〕adafruit〔t1〕