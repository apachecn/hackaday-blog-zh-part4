# 随着书本的声音摇滚起来

> 原文：<https://hackaday.com/2018/11/14/rock-out-to-the-written-word-with-booksound/>

通过他的最新项目，[Roni Bandini]同时给了世界一种新型的有声读物和音乐。传统的有声读物基本上相当于成人让某人给你读睡前故事，但是 [BookSound 实际上将书面文字转化为电子音乐](https://hackaday.io/project/162262-booksound)。你不能向你的朋友吹嘘，事实上，你*已经*读过那本受欢迎的新小说，但至少你可能会随着它起舞。

[![](img/3dcc61105bee7a12f6cfee856be6df09.png)](https://hackaday.com/wp-content/uploads/2018/11/booksound_detail.jpg)【Roni】说他还在完善词到音乐的映射，所以休息后视频中显示的结果还是有点粗糙。但即使在这些早期阶段，不可否认这是一个非常独特的项目，我们很高兴看到它从这里走向何方。

在这个看起来经典的 3D 打印外壳中，有一个树莓皮、一个有机发光二极管显示器以及按钮和开关，它们构成了该设备的控制范围。在机械臂的末端是一个标准的 Raspberry Pi 相机模块，它可以让 BookSound 鸟瞰要演唱的书籍。

要把你最喜欢的书变成电子节拍，只需打开它，把它放在 BookSound 的注视下，然后按下前面的按钮。因为 Raspberry Pi 并不完全是一个发电站，它需要大约两分钟来扫描页面，执行光学字符识别(OCR)，并在您开始听到任何东西之前编写轨道。

如果你想知道将文字转化为音乐的秘诀是什么，[Roni]还没有准备好分享他的源代码。但是他能够给我们一些关于 BookSound 内部情况的高层次解释。例如，为了生成歌曲的 BPM，软件会计算页面上每段有多少单词:因此，段落较短的书会有更快的节奏，以匹配作者通过思想移动的速度。同样，鼓踢是根据每个段落中音节的数量生成的。将来，他打算通过文本到语音引擎运行页面上的常用词，并将它们插入节拍中，从而添加“歌词”。

我们已经看到了过去在 Raspberry Pi 和[上 OCR 的实际应用，甚至类似的书籍扫描安排](https://hackaday.com/2018/03/02/diy-text-to-speech-with-raspberry-pi/)。但是没有什么比以前的书更好的了，在这一点上，这真的很有意义。

 [https://www.youtube.com/embed/FBNsJvDjteI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FBNsJvDjteI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

