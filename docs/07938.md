# 用卡带播放器 Synth 播放岁月

> 原文：<https://hackaday.com/2020/10/01/reel-in-the-years-with-a-cassette-player-synth/>

变速播放卡带播放器已经是最酷的产品了。除此之外，如果不拔掉磁头，手动在那些光滑的棕色磁带上运行，你怎么能对磁带感兴趣呢？当然，你可以在大多数播放器上改变播放速度，只要你能到达微调壶。但是真正的变速播放器能做出更好的合成器，因为改变速度要容易得多。你可以用任何可以录在磁带上的东西来创作音乐，包括单调。

[【schollz】制作了一个磁带合成器，只不过是一个变速播放卡带播放器、一个 Arduino、一个 DAC 和几根连接它们的电线](https://schollz.com/blog/tape-synth/)。它是这样工作的:[schollz]在磁带上录制一个长的单个音符，然后通过 MIDI 合成器的电压来改变回放速度，从而使用该录音播放不同的音符。

为了从一个 synth 到另一个 synth，[schollz]建立了一个服务器，将 MIDI 电压转换为串行，并将其发送到 Arduino。然后，DAC 将它们转换成模拟信号，供磁带播放机使用。所有的代码都可以在项目网站上找到，[schollz]甚至会告诉你在哪里添加 Vin 和一行到磁带播放器中。休息后请欣赏演示。

侵入卡式录音机的方法不止一种。你也可以强迫他们播放全动态的彩色视频。

 [https://www.youtube.com/embed/LdBik_Zlwy0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LdBik_Zlwy0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通路〔t0〕adafruit〔t1〕