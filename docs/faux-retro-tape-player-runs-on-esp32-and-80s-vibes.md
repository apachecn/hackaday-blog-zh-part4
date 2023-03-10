# 仿复古“磁带”播放器运行在 ESP32 和 80 年代的氛围

> 原文：<https://hackaday.com/2022/06/23/faux-retro-tape-player-runs-on-esp32-and-80s-vibes/>

乍一看，【Max Kern】打造的这个[华丽复古风格的音频播放器绝对可以当正品。但你仔细一看，就会发现它正在播放的“磁带”实际上是在 320 x 240 IPS 显示器上运行的动画，前面的播放和倒带按钮不是过去笨重的机电事务，而是巧妙地重新利用了 MX 键盘开关。](https://hackaday.io/project/185994-diy-retro-audio-player)

[![](img/493d767a24d1b1055a7908f6385b7ea3.png)](https://hackaday.com/wp-content/uploads/2022/06/retroplayer_detail.jpg) 现在你可能已经意识到这款播放器比你最初想象的要小很多，这反过来意味着它甚至连外壳都是现代制造的。虽然它可能完美地封装了一件 20 世纪 80 年代消费电子产品的外观和感觉，但它是在一台完全现代的桌面 3D 打印机上喷射出来的。

即便如此，[Max]确保在 CAD 设计中包括拔模角度和独特的分隔线，这样表壳*看起来*就像是注射成型的。遵循类似的逻辑，他决定不使用现代充电电池组为电子设备供电，而是选择一套更适合时代的 AA 电池。

在硬件方面，定制的 PCB 是一个 ESP32 WROOM，一个 MAX98357A I2S 音频放大器，一个 FT231XS USB 到串行芯片的家园，有足够的无源器件和调节器来让他们都吃饱喝足。ESP32 拥有足够的计算能力来咀嚼 MP3 文件，这些文件可以通过播放器侧面内置的 SD 插槽方便地加载。由于播放器实际上是为有声书设计的，板载播放仅限于单声道扬声器；虽然有一个 3.5 毫米的音频插孔，可以在内置扬声器无法完成任务时插入一对耳机。

[![](img/70671fb5a8079ef10e0e54695904b52b.png)](https://hackaday.com/wp-content/uploads/2022/06/retroplayer_detail2.jpg)

休息后查看视频，了解播放器是如何组装的，以及其简单的三按钮用户界面的演示。它看起来使用起来很愉快，尽管缺乏快进和倒带音效让我们有点惊讶，因为它对细节的关注无可挑剔。我们将假设有一些技术限制，使得这特别难以实现，并且他们的缺席目前使[Max]夜不能寐。

尽管最终产品令人印象深刻，但我们不能说它是一个惊喜。坦率地说，在这一点上，我们对[马克斯]的期望不会更低。他的自适应有机发光二极管宏垫在 2020 年让我们惊叹不已，他的 [ZeroBot 仍然是我们见过的 DIY 两轮机器人中最光滑的设计之一](https://hackaday.com/2017/05/31/zerobot-is-as-simple-as-it-gets/)。

 [https://www.youtube.com/embed/C0gdGp54DQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C0gdGp54DQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

