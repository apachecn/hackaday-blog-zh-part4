# 一个你可以用浏览器控制的 SNES 音乐播放器

> 原文：<https://hackaday.com/2021/08/08/a-snes-music-player-you-can-control-with-a-browser/>

在模拟器或基于软件的播放器上听 chiptunes 很好，但有时你必须拥有真正的硬件魅力。[Kazhuu]就是这样一个有这种感觉的爱好者，他着手为 SNES chip tunes[开发一个可以通过浏览器控制的硬件播放器。](https://github.com/Kazhuu/spc-player)

该版本依靠 Arduino 微处理器来控制 SNES 音频处理单元(APU)，其特点是由索尼生产并由 Ken Kutaragi 设计的任天堂 S-SMP。是的，PlayStation 之父在超级任天堂中设计了有能力的 wavetable 合成芯片，也是这个硬件使[Kazhuu]的项目与现代硬件接口。

Arduino 的 IO 线连接到 APU，歌曲数据可以通过串行连接到 PC 的管道输出到 Arduino。这可以通过 Python 脚本来处理，或者更直观地通过基于浏览器的前端来处理。它使用 WebUSB 从浏览器获取输入，然后通过 USB 串行连接将数据发送到 Arduino。

这是一个简洁的演示，既演示了如何使用老式的任天堂声音硬件，又演示了如何编写现代浏览器应用程序来与嵌入式系统一起工作。如果你是一个 SEGA 的孩子，你可能会更喜欢这个建筑而不是 T1。休息后的视频。

 [https://www.youtube.com/embed/2sleZUMQwSA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2sleZUMQwSA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

