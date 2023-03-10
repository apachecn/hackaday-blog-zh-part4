# super co 2022:Mooneer Salem 搭配 ESP32 火腿

> 原文：<https://hackaday.com/2022/12/28/supercon-2022-mooneer-salem-goes-ham-with-an-esp32/>

自 21 世纪初获得业余无线电操作员执照后，你倾向于开始考虑将你对无线电的热爱与其他才能结合起来。在 Hackaday Supercon 2022 上的一次 20 分钟的演讲中，[Mooneer Salem]讲述了一个这样的激情项目的故事，该项目将软件和无线电结合起来，使数字业余无线电调制器小型化。

[Mooneer]是一名软件开发人员，参与了一个名为 FreeDV(免费数字语音)的[项目，](https://github.com/drowe67/freedv-gui)是一种用于高频无线电的数字语音模式。FreeDV 首先压缩数字音频流，然后将其转换为通过无线电发送的调制方案。吸引力在于，这可以理解为非常低的信噪比，并包括元数据和数字信号带来的所有其他细节。

传统上，除了两个声卡之外，这需要一台计算机来压缩音频和调制信号。一张卡处理耳机的音频输入和输出，另一张卡处理收音机的音频输入和输出。[David Roew]和[Rick Barnich]开发了 SM1000，这是一款基于 STM32F4 微控制器的便携式 FreeDB 适配器。但是，闪存空间越来越少，成本超出了他们的预期。

[Mooneer]喜欢 SM1000 的开放式固件和开放式硬件模型，并希望重新审视这一想法。使其更易于使用，添加新功能，最重要的是，降低成本。ESP32 是一个显而易见的选择，因为它便宜，符合他的所有条件。他最终选定了 ESP32-S3，因为标准的 ESP32 不具备实时运行所需的性能。TLV320 开发板非常昂贵，因此他自己开发了这种体验，这种态度我们很多人都有同感。

在处理了几天 I2S 的问题后，他重新安装了电路板，试图解决只能听到 60 赫兹噪音的音频问题。假设是电磁干扰问题，他重新布线，调整元件，并增加更多的过孔。然而，即使在 respin 之后，问题仍然存在，他意识到 TLV320 有一个环回模式，这毕竟是一个软件问题。

结果是 ezDV 在 TAPR 开放硬件许可和 GNUv3 许可下在 GitHub 上拥有[所有的代码和板文件。它支持 FreeDV 五种模式中的三种(不支持 2020 或 700C)。不支持 2020 是有道理的，因为 2020 使用 LPCNet 神经网络将 8 kHz 的音频转换为 1600 Hz。这需要一台有 AVX 支持的相当强大的计算机。](https://github.com/tmiw/ezDV)

[Mooneer]呈现了一个关于创造一些有据可查和可复制的东西的旅程的美丽故事。如果你正在研究数字广播，也许这是一个很好的起点。

 [https://www.youtube.com/embed/3FlFp1ZS7GE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3FlFp1ZS7GE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

