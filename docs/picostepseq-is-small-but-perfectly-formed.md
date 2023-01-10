# PicoStepSeq 很小，但是格式完美

> 原文：<https://hackaday.com/2022/08/20/picostepseq-is-small-but-perfectly-formed/>

Raspberry Pi Pico 是您可能会称之为当前的主板，这要归功于它的经济性、功能和在组件短缺期间的持续可用性。我们已经看到了许多使用它的伟大项目，最近浮出水面的是[todbot]的 [PicoStepSeq，一个极其紧凑的 MIDI 音序器](https://github.com/todbot/picostepseq)。

所有组件都安装在一个 PCB 上，序列器的八个步骤由一排集成 led 的按钮选择。接口是通过 SSD1306 有机发光二极管，还有一个旋转编码器。软件由 CircuitPython 提供，输出通过 3.5 毫米 TRS 插孔传输。最后，整个包裹在一个 3D 打印的外壳中。

其结果是一个音序器几乎可以成为一个独立的产品，我们认为任何对电子音乐感兴趣的人都应该可以很容易地制造出来。在链接的知识库中可以找到构建你自己的库所需的所有文件和信息，他在网上发布了一条推文和一段视频，我们已经将这段视频嵌入到休息时间的下方。

> 我做到了！在 2 周内，我为一个产品创意设计、编码、PCB 制作和 CAD 了一个外壳:一个微型的基于 Pico 的 MIDI 步进序列器“PicoStepSeq”。Thx to [@johnedgarpark](https://twitter.com/johnedgarpark?ref_src=twsrc%5Etfw) 获取灵感& [@adafruit](https://twitter.com/adafruit?ref_src=twsrc%5Etfw) 获取原型工具【https://t.co/WpGZIhJpHv[pic.twitter.com/kek4U2Y4mq](https://t.co/kek4U2Y4mq)
> 
> —托德·库尔特(@托德·博特)[2022 年 8 月 19 日](https://twitter.com/todbot/status/1560676715424141313?ref_src=twsrc%5Etfw)