# 采用音频 DSP 的小型 SDR 接收机

> 原文：<https://hackaday.com/2020/02/01/a-mini-sdr-receiver-using-an-audio-dsp/>

软件定义无线电(SDR)是无线电领域最激动人心的前沿，它将所有信号功能从模拟域转移到数字域。使用 SDR 技术的无线电可以令人惊讶地简单易懂，而[Ray Ring]的小型 SDR 接收器[成功地将这一点与音频 DSP](https://circuitsalad.com/2020/01/06/compact-si5351-based-sdr/) 的新颖使用相结合，而不是使用计算机来执行其 SDR 功能。

前端是一个足够传统的直接变频设计，Si5531 时钟发生器向用作混频器的 [TS3A5017](http://www.ti.com/product/TS3A5017) 模拟开关提供 I 和 Q 相移本振信号。意想不到的是，LTC6252 运算放大器用作 RF 放大器，但特殊部分出现在 I 和 Q 基带信号经过滤波之后。该接收机的 SDR 部分是一个音频 DSP，但它可能不是一个直接的选择。 [Spin Semiconductor FV-1](http://www.spinsemi.com/products.html) 是一款专用于音乐效果盒的数字混响芯片，但它具有内部 DSP 内核可以从外部 rom 访问自定义代码的功能。[Ray]编写了自己的代码来解调 AM、USB 和 LSB 信号，而不是音乐效果，并使用设备的左右音频通道来处理 I 和 Q 正交信号。使用一个专用芯片来做它的设计者从来没有打算过的事情，这给了它一个好黑客的本质，我们对他在音乐效果中发现 SDR 的潜力印象深刻。请在休息时间下方的视频中听听它的实际效果。

同时，如果像这样的接收器的操作对你来说是一个谜，[我们在 2017 年](https://hackaday.com/2017/05/16/if-the-i-and-q-of-software-defined-radio-are-your-nemesis-read-on/)出版了一本方便的入门书。

 [https://www.youtube.com/embed/kSXi0DoSYBs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kSXi0DoSYBs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示。