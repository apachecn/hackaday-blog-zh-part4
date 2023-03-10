# Flash: Arduino Vidor FPGA 指令登陆法国

> 原文：<https://hackaday.com/2018/10/14/flash-arduino-vidor-fpga-instructions-hit-france/>

如果你会说法语，并且有一台 Arduino Vidor 4000，你很幸运，因为有一些好消息。好消息是，终于有了一些关于如何自己配置板载 FPGA 的内部信息。然而坏消息是它相当稀少。如果你的高中法语达不到要求，总有[谷歌翻译](https://translate.google.fr/translate?hl=fr?sl=auto&tl=en&u=https%3A//systemes-embarques.fr/wp/archives/mkr-vidor-4000-programmation-du-fpga-partie-1/)。

我们已经知道了一些。你需要 Quartus，Altera——呃，Intel 的 FPGA 设计工具——我们也知道 GitHub 上的[样本项目。新信息不使用传统的 Verilog 或 VHDL，而是使用原理图捕获，但这没关系。所有的设计条目都集中在同一个地方，所以应该很容易适应你选择的语言。事实上，在](https://github.com/vidor-libraries/VidorFPGA)[第二部分](https://translate.google.fr/translate?hl=fr?sl=auto&tl=en&u=https%3A//systemes-embarques.fr/wp/archives/mkr-vidor-4000-programmation-du-fpga-partie-1/)中，他们展示了一些原理图和一些 Verilog。不过，谷歌翻译在代码注释方面确实有点麻烦。如果你想要更结实的东西，有一个使用 [Verilog 输出视频帧](https://translate.google.fr/translate?hl=fr?sl=auto&tl=en&u=https%3A//systemes-embarques.fr/wp/archives/mkr-vidor-4000-programmation-du-fpga-partie-1/)的例子。

真正的问题是:如何在电路板上不动手术的情况下将比特流导入 FPGA？有一个 [Java 应用程序](https://systemes-embarques.fr/wp/wp-content/uploads/2018/09/ReverseByte.zip) (Zip 下载)可以为你构建一个. H 文件。在您的草图中包含它将导致 Arduino 为您加载 FPGA。关于它是如何工作的，仍然没有太多的细节——我们认为几乎有一个 FPGA 引导加载程序保持加载，然后像这样获得其余的配置。

此外，结尾还有一句警告:

> 在任何情况下都不应该重新配置 SAMD21 输出的 PA20 端口。这一个已经被 FPGA 用作输出。

我们可以想象还有其他的陷阱，所以如果你开始尝试，你就有可能会毁掉你的 Arduino。

尽管如此，这仍然是个好消息！我们一直渴望玩板载 FPGA，这应该回答了足够的问题，以解决其余的细节。所有的例子，包括一个 DVI 输出的例子，都链接在[一个下载页面](https://translate.google.fr/translate?hl=fr?sl=auto&tl=en&u=https%3A//systemes-embarques.fr/wp/archives/mkr-vidor-4000-programmation-du-fpga-partie-1/)上。

如果你想[了解更多关于硬件](https://hackaday.com/2018/07/30/hands-on-with-new-arduino-fpga-board-mkr-vidor-4000/)的信息，我们已经介绍过了。我们也有一些 [FPGA 训练营](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/)，可以帮助你开始使用 FPGA。