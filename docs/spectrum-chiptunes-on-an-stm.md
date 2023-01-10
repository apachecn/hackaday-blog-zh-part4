# STM 上的频谱芯片调谐

> 原文：<https://hackaday.com/2019/06/07/spectrum-chiptunes-on-an-stm/>

在 Hackaday，我们中的一些人喜欢用一些 chiptune 音乐作为许多美好时光的背景。创建 chiptunes 的真实方法当然是原始硬件，但在 2019 年，使用现代计算机上的仿真器来这样做要常见得多。不过，这款电脑不一定要配备高端处理器和桌面操作系统，正如[Deater]在 STM32L46G 探索板上用他的[ZX spectrum chip tune 播放器向我们展示的那样。](http://www.deater.net/weave/vmwprod/hardware/stm32l476_chiptune/)

他告诉我们，这个项目的动力来自于在教学生编写简单的正弦波音乐播放器时，他已经有了在 [Raspberry Pi](https://hackaday.com/2017/06/11/multifunction-raspberry-pi-chiptune-player/) 和 [Apple II](https://hackaday.com/2018/12/05/apple-ii-megademo-is-countin-cycles-and-takin-names/) 上模拟经典 AY-3-8910 声音芯片的代码，他决定将其移植到 STM32L476 开发板上。早期版本使用内部 DAC，但经过改进后，可以将 I2S 数据发送到外部 DAC。[代码可以从 GitHub](https://github.com/deater/vmw-meter/tree/master/stm32L476) 获得(令人困惑地隐藏在一个 LED 驱动程序的代码中)，我们在下面附上了它播放一些 chiptune goodness 的视频。

当然，Sinclair chiptunes 并没有获得所有的关注。也有很多任天堂、T2、世嘉和 T3 的玩家。你可能还会从他的非 chiptune 作品中认出[Deater]，[将门户移植到苹果上][](https://hackaday.com/2017/01/12/portal-ported-to-the-apple-ii/)。

 [https://www.youtube.com/embed/lRYMZZaOo5E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lRYMZZaOo5E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

