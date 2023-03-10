# RAM 拨弄把 VGA 转换器变成视频合成器

> 原文：<https://hackaday.com/2021/05/25/ram-fiddling-turns-vga-converter-into-video-synth/>

如果你对电路弯曲视频感兴趣，但不知道从哪里开始，那么[优秀的指南【LoFi Future】已经提出，修改便宜且容易获得的 GBS-8100](https://www.lofifuture.com/gbs8100-diy-video-synth-project) VGA 到复合转换器将是一个伟大的第一步。虽然我们不认为这是一个简单的修改，但下面的电路文档和演示视频尽可能地让新玩家更容易理解。

[![](img/2e021ecf0a9e8d8d1b9b4bca3d460f2f.png)](https://hackaday.com/wp-content/uploads/2021/05/gbsglitch_detail2.jpg)

Some soldering will be required…

虽然其他视频转换器都有更难使用的一体化芯片组，但[LoFi Future]解释说，GBS-8100 上单独的 EM636165TS DRAM 芯片提供了一个理想的位置，可以利用它进行一些技术破坏。通过绘制引脚图，并研究视频输出如何因接地或相互连接而受到破坏，他已经能够为不同的效果提供相当可重复的“配方”。

在最基本的形式中，一旦你把 DRAM 芯片的管脚焊接到插板接口上，技术上你就完成了。但[LoFi Future]更进一步，将 GBS-8100 与一个单独的复合 VGA 转换器配对。这以反馈循环和色调调整的形式提供了一些额外的效果，但更实际的是，允许设备处理输入和输出上的复合。这是一个很大的硬件塞进外壳，但由于像印刷面板图形的小接触，最终产品看起来非常专业。

除了偶尔改装的 NES Zapper ，我们看到的大多数[电路弯曲硬件都是音频种类](https://hackaday.com/2019/06/08/circuit-bending-those-adorable-voices/)。但是有了像这样的项目和我们去年报道的 MIDI 控制的 SNES[作为灵感，我们可能会看到天平的平衡。](https://hackaday.com/2020/09/19/controlling-a-broken-super-nintendo-with-midi/)

 [https://www.youtube.com/embed/zMlJFY3scrQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zMlJFY3scrQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

