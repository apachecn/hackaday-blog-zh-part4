# 老式视频处理器的示波器触发器

> 原文：<https://hackaday.com/2022/10/18/an-oscilloscope-trigger-for-vintage-video-processors/>

正如[ukmaker]最近在设计新的显示界面时发现的那样，在复古电脑上工作很少是直截了当的。他们的示波器在触发老式视频电路产生的视频信号时遇到了问题，所以他们为逆向计算机创造了[视频触发器。](https://www.instructables.com/Video-Trigger-for-Retrocomputers-Using-TMS99282912/)

德州仪器(TMS9918 视频显示控制器广泛应用于 20 世纪 80 年代的游戏控制台和家用电脑，从著名的 ColecoVision 到德州仪器(TI)自己的 TI-99/4。尽管有大量的复古计算遗产，但该芯片的视频输出(原因不明)与 Hantek DSO1502P 示波器不太兼容。如果对视频信号没有更好的理解，就很难将该芯片用于新的 TFT 显示器，这种显示器是为具有更宽 NTSC 容差的 CRT 电视设计的。

也许一个不同的示波器可以解决这个问题，但是[ukmaker]感觉示波器需要一个外部触发信号。视频触发项目使用 LM1881 同步分离器从老式视频芯片中梳理出水平和垂直同步信号，输出通过管道进入 ATmega 328P。除了少量分立元件，ATmega 还帮助用户选择哪条线作为触发帧，以及水平同步信号的斜率。微型有机发光二极管显示器使配置变得容易。

如果这激起了你的兴趣，[ukmaker]还在 GitHub 上写了一篇很棒的文章，介绍了所有血淋淋的细节。也许它会对你下一次的老式计算有所帮助。拥有合适的工具可以让一切变得不同，就像这个[自制逻辑表，用于业余电子故障排除](https://hackaday.com/2021/01/28/logic-meter-aims-to-make-hobby-electronics-troubleshooting-easier/)。或者如果你想知道更多关于模拟 NTSC 视频的神秘属性，[我们也已经报道过了](https://hackaday.com/2014/07/15/demystifying-ntsc-color-and-progressive-scan/)。