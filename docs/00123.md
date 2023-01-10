# 将廉价的蓝牙扬声器变成音频接收器

> 原文：<https://hackaday.com/2018/07/23/turn-a-cheap-bluetooth-speaker-into-an-audio-receiver/>

廉价的蓝牙扬声器有各种不同的形状和颜色，它们可以让你方便地播放音乐，例如从你的手机上播放。对于[mcmchris]来说，他们有一个明显的缺点:虽然他们中的大多数都有一些辅助输入端口作为替代音频源，但他们通常缺少一个音频输出端口，让他可以将音频发送到更令人愉快的大扬声器音响系统。幸运的是，这是一个可以用钢丝钳和烙铁解决的问题，所以他简单地把他的廉价扬声器变成了蓝牙音频接收器。

打开扬声器后，[mcmchris]发现了一个围绕 BK8000L 芯片构建的常规 F-6188 蓝牙音频模块，音频插孔连接到芯片的 aux 输入引脚。仔细看看 PCB，解决方案似乎很明显:切断与芯片的 aux 输入引脚的连接，并将音频插孔与音频信号本身平行连接。经过反复试验，板载运算放大器的输出引脚似乎为他闪亮的新输出插孔提供了最佳音频信号。休息之后，你可以在视频中看到更多关于演讲者内心生活的细节和演示——用西班牙语。

如果这个概念对你来说很熟悉，我们以前确实见过一种非常类似的方法为谷歌 Home Mini 配备一个音频输出插孔。当然，另一种选择是[自己制作一个合适尺寸的蓝牙扬声器](https://hackaday.com/2017/12/08/bluetooth-speaker-in-a-bag/)。

 [https://www.youtube.com/embed/awc3ytQ-C28?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/awc3ytQ-C28?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

