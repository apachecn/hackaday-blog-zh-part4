# 潜艇黑客用 Arduino Nitrox 分析仪

> 原文：<https://hackaday.com/2018/11/03/arduino-nitrox-analyzer-for-the-submarine-hacker/>

对于不在水下度过空闲时间的 Hackaday 读者来说，nitrox 是氮和氧的混合物，很受潜水者的欢迎。与大气相比，氮氧化物具有更高的氧气浓度；这不仅能让潜水员在水下呆更长时间，还能降低患减压病的风险。当然，当摆弄你呼吸的气体比例时，会有不可忽视的死亡风险，所以氮氧潜水需要特殊的训练和设备来确保气体混合物是正确的。

潜水员可以用一个便携式分析仪来检验他们的氮氧气瓶中的氧氮比，尽管正如你所料，它们并不便宜。但是如果你对自己的黑客技术有信心，[【eun jae Im】可能会为那些希望节省一些现金的潜水员提供解决方案](https://ejlabs.net/arduino-oled-nitrox-analyzer/)。他发明了一种基于 Arduino 的氮氧化物分析仪，其制造成本远低于商用设备。

现在，在你点燃火炬之前，我们应该清楚:最终，这个设备的准确性和安全性取决于所使用的氧传感器的质量。[Eunjae]并不建议您为此构建一个桶底传感器，事实上，它链接到一个用于商业 nitrox 分析仪的替代传感器，以此来验证该装置是否能够胜任任务。不利的一面是，光传感器就要 80 美元。如果你想买更便宜的东西，你要自担风险。

有了合适的传感器，这个项目实际上可以归结为为它建立一个接口和外壳。[Eunjae]使用的是 Arduino Nano，128×64 有机发光二极管屏幕，电池放在坚固的防水外壳中。他还在氧气传感器和 Arduino 之间添加了一个 ADS1115 16 位 DAC，以便在 I2C 上空快速准确地读取数据。组装好硬件后，校准该设备就像把它拿到外面并确保获得 20.9%的氧气读数(大气正常值)一样简单。

虽然[Eunjae]总体上对他的分析器很满意，但他确实看到了一些在未来版本中可以改进的地方。这种外壳体积庞大，相当不美观，这可以通过定制的 3D 打印外壳来解决(尽管防水可能是一个问题)。他还说，他使用 9V 碱性电池的唯一原因是因为他手头有电池，一个小的可充电电池组将是一个更优雅的解决方案。

我们可以大胆地说，大多数 Hackaday 的读者并不热衷于潜水。不管是好是坏，我们是那种呆在游泳池浅水区的人。但是当我们中的一员真的潜入水下时，[他们似乎真的会全力以赴。](https://hackaday.com/2016/08/23/diy-pressure-regulator-for-exciting-scuba/)

 [https://www.youtube.com/embed/VeIdiBIsKHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VeIdiBIsKHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

