# RPi Python 库包含复古的 Chiptunes 和语音

> 原文：<https://hackaday.com/2021/09/09/rpi-python-library-has-retro-chiptunes-and-speech-covered/>

经典的 SP0256-AL2 语音芯片在这些页面上出现过几次，如果你以前没有见过实际的部分，你几乎肯定听过最终的音频输出。来自多产的逆向计算爱好者[Nick Bild]的最新 Python 库为 Raspberry Pi 平台带来了旧芯片的[乐趣，并增加了额外的技巧；支持古老的](https://github.com/nickbild/gi-pi) [AY-3-8910 发声器](https://en.wikipedia.org/wiki/General_Instrument_AY-3-8910)。

SP0256-AL2 芯片使用[音位变体系统](https://en.wikipedia.org/wiki/Allophone)产生模糊可识别的语音。音位变体有点像语音音频的小块，当顺序再现时，产生可理解的音素，形成语音的基础。芯片需要一个外部设备以固定的速率给它输入音位变体，这是他的 [Gi-Pi 库](https://github.com/nickbild/gi-pi)的工作。

这种语音合成技术基于[线性预测编码](https://en.wikipedia.org/wiki/Linear_predictive_coding)，用于实现人类声道模型。这与第一代 GSM 数字移动电话使用的编码方法相同，实现了一个被称为[全速率](https://en.wikipedia.org/wiki/Full_Rate)的系统。LPC 编码器和 LPC 解码器都存在于手机上。LPC 编码器接收来自用户的音频，将其分解成微小的语音组成部分，然后简单地发送代表音频块的代码，而不是实际的音频。显然，还发送了一些参数来调整接收端的模型。因此，实际的解码端与 AY-3-8910 和相关设备所做的并无太大不同，只是用户必须预先创建音频块列表，并以芯片要求的速率向芯片提供数据。

硬件方面，[Nick]没有记录他的试验板构建，但 SP0256-AL2 相当容易驾驶。只需将 Pi 的 3.3V 逻辑电平转换到芯片的 5V 域，然后用几个并行 GPIOs 对其进行位处理。然后，PCM 音频输出经过低通滤波，并馈入音频混频器和功率放大器。

AY-3-8910 的处理方式与此类似，只是它包含自己的 DAC 模块，因此输出已经是模拟的，只需将模拟输出直接馈入上述的共享混频器即可。

我们之前已经展示过 AY-3-8910 声音芯片，这个[简单的黑客，将 Arduino 变成 MIDI 设备](https://hackaday.com/2019/07/30/chiptunes-via-usb-midi-with-the-ay-3-8910/)。查看莫扎特的歌剧《魔笛》中的《夜之女王》咏叹调的甜美 chiptunes 版本。

休息后的视频给出了一个(有点短的)演示，演示结果是你可以预期的语音音频，就好像你还不知道一样。

 [https://www.youtube.com/embed/u-AI8lnBwgg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u-AI8lnBwgg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

