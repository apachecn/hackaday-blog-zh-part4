# 简单的通用调制解调器有助于从磁带上保存和加载数据

> 原文：<https://hackaday.com/2022/07/27/simple-universal-modem-helps-save-and-load-data-from-tape/>

在家用电脑革命的早期，数据通常保存在磁带上。更妙的是，如果你用立体声播放这些磁带，它们会发出巨大的噪音，因为数据是以音频格式存储的。[Anders Nielsen]生产的简单通用调制解调器也是以类似的方式工作，将数据转换成音频，反之亦然。

该项目包括一个电路，用于将数据调制成音频，并将音频解调回数据。它是“通用的”,因为[Anders]将它设计成尽可能与格式无关。不管你是想把数据存储在数字录音机、卡式录音机，还是老式的卷对卷机上，都没有关系。这个版本应该可以很好地运行在所有这些版本上！

在调制方面，它设计得尽可能模拟友好。它不只是吐出粗糙的方波，而是将它们调制成谐波更少的平滑正弦波。在解调方面，它有一个 LM393 比较器，可以读取磁带上的数据，并吐出干净的方波，便于数字电路解码。

如果您发现自己正在尝试从磁带上恢复旧数据，或者为了一个逆向计算项目而向它们写入数据，那么这个版本可能正是您所需要的。[Anders]甚至在一个有用的 YouTube 视频中用一个旧的卷对卷卡座演示了它的使用。

很久以前确实有一些奇怪的存储数据的方法。问问 IBM 就知道了。休息后的视频。

 [https://www.youtube.com/embed/k8hlYr6N3Ls?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/k8hlYr6N3Ls?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

