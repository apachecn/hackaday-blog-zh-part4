# Ioalieia 的怪异声音:ESP32/阀门/模拟混合电路雕塑

> 原文：<https://hackaday.com/2022/01/15/the-eerie-sounds-of-ioalieia-an-esp32-valve-analog-hybrid-circuit-sculpture/>

我们已经有一段时间没有电路雕塑作品了，所以这里有[【ioalieia】一个可爱的数模混合声音雕塑](https://hackaday.io/project/183534-ioalieia)由【Eirik Brandal】创作。

[![](img/c4982bbc4740a41bcae0ae639698124c.png)](https://hackaday.com/wp-content/uploads/2022/01/4554111641816489885.png)

Tidy straight lines. Nice job!

该节目的主持人是 ESP32 模块，它产生音频方波，并馈入一个 [MCP4251](https://www.microchip.com/en-us/product/MCP4251#document-table) 数字电位器。从那里，它被馈入一个 [AS3320](http://www.alfarzpp.lv/eng/sc/AS3320.pdf) 电压控制滤波器(VCF)，来自拉托维亚的[阿尔法](https://www.alfarzpp.lv/eng/sc/semiconductor.php)(这对我们来说是新的，尽管他们制造电子产品已经有 60 年了！)这是一个有趣的设备，它有四个可独立配置的滤波器元件，带有用于频率控制和谐振的电压控制输入。VCF 的输出然后被馈入 6n2p(苏联相当于 [12ax7](https://en.wikipedia.org/wiki/12AX7) )双三极管真空管，专门针对音频应用。

经过适当失真滤波的方波随后进入[普林斯顿技术公司 PT2399](http://www.princeton.com.tw/Portals/0/Product/PT2399_1.pdf) 回声处理器芯片，该芯片采用数字结构，使用预期的 ADC/RAM/DAC 信号链来实现音频回声效果。与 VCF 一样，回声深度可以在 ESP32 的命令下通过 digipot 进行调制。为了增加一点光彩，真空管输出反馈到 ESP32，由内部 ADC 消耗，并通过一些 PWM 控制的 led 变成灯光秀。很可爱。

echo 芯片的最终音频输出然后通过一对功率约为 5 W 的 LM380 放大器馈入扬声器。如果你问我们，这听起来很好，软件可通过 Wi-Fi 配置，让这个雕塑有很多可调整性。

当然，电路雕塑有各种形状和大小，至少不能不提[一个雕塑时钟项目](https://hackaday.com/2021/11/10/a-breathtaking-circuit-sculpture-clock/)，当我们谈到它时，这里是去年的 [Remoticon 电路雕塑工作室](https://hackaday.com/2020/12/03/remoticon-video-circuit-sculpture-workshop/)。

 [https://www.youtube.com/embed/6p7aZKGtWz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6p7aZKGtWz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

