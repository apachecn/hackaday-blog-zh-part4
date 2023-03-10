# SBC 接口生态系统的状态，是时候设计一个标准了吗？

> 原文：<https://hackaday.com/2022/10/05/the-state-of-the-sbc-interface-ecosystem-is-it-time-to-design-a-standard/>

当谈到单板计算机时，我们被宠坏了，无论它们是基于微控制器还是能够运行 GNU/Linux 等操作系统的更强大的 SoC。它们可以从 Arduino、Adafruit 或 Raspberry Pi 等知名品牌获得，也可以从拥有大量不同架构的廉价远东模块的狂野西部获得。

每个人都有自己最喜欢的，随之而来的是一个操作系统和软件开发环境的生态系统。这些板子还有另一个进化的方面。其中某些已经成为硬件外设的事实上的接口连接器标准。这些标准有意义吗？让我们谈谈那个。

## 事实上的标准是如何产生的？

在大多数情况下，接口标准是专门创建它的成果。以 USB-C 端口为例，这不是因为制造商决定在机器上安装一个带电源功能的可逆高速数据端口而产生的，而是行业联盟多年经验和工作的结果。

[![A car cigarette lighter](img/87ef0d262b503f934742152bfa8429c4.png)](https://hackaday.com/wp-content/uploads/2022/09/Zigarettenanzuender_04_fcm.jpg)

How on earth did this become a power standard?

不过，有时接口标准会偶然出现。从任何标准来看，汽车附件插座都是一个非常糟糕的电源连接器系统，它起源于几十年前，当时是一个电子点烟器的插座。因为没有其他方便的方法来获取汽车中的 12 V 电源，所以它成为了少数可用的电子车载附件的电源，并从此演变成了标准的汽车电源插座。奇怪的是，许多汽车附件插座现在已经不适合它们最初的用途，不再设计成能承受点烟器元件的热量。

所以我们来看看单板计算机上的连接器。几乎所有的接口都有一个扩展连接器，目的是在一个地方尽可能多地引出可用的接口。有些设计得很好，有些则不太好，但没有一个设计得像 USB 插座那样独立于特定硬件，并且考虑到所需应用的便利性。相反，它们留给了电路板的设计者，他们可能不期望该设备成为广泛采用的标准，因此可能不会提前考虑如何使用他们的发明。

## 这些都不像其他的

如果我们被要求说出一些其接口已经成为非预期的事实上的标准的主板，我们最终得到的那些不会让你们大多数人感到惊讶。最初的 Arduino，树莓 PI，Adafruit Feather，也许是树莓 Pi Pico，也许是 BeagleBone，还有一个我们越来越多看到的，BBC micro:bit。值得花一分钟单独看一看，找出我们喜欢它们的什么，不喜欢它们的什么。

[![An Arduino Uno R3](img/7da2fb85bdd20687ef77f3aca4dbcde3.png)](https://hackaday.com/wp-content/uploads/2022/09/interface-unoR3.jpg)

The familiar Arduino Uno with its two rows of shield connectors.

他们的祖师爷一定是 Arduino。我们不知道是否是第一块板子给了我们盾牌的想法，但肯定是它普及了它们。在 Arduino 出现之前，主板通常会在带有 I/O 线的头部旁边提供一个原型制作区域，子板可能会连接到该头部，Arduino 让一系列附加板在一个定义好的生态系统中扎根。

我们喜欢 [Arduino 扩展引脚排列](https://docs.arduino.cc/hardware/uno-rev3),因为它将不同类型的接口组织在一起，并按数字顺序排列，我们也喜欢它使用廉价的 0.1”引脚接头，但它的尺寸和对两组相距如此之远的接头的需求看起来明显笨拙和过时。不要让我们从[奇数行偏移](https://web.archive.org/web/20180926125226/http://forum.arduino.cc/index.php?topic=22737.msg171839#msg171839)开始。尽管如此，我们可能还需要很长时间才能摆脱经典的 Arduino shield，因为还有很多可用的，但在 2022 年，这是一个新设计的合理选择吗？我们不这么认为。

![A Pi 4 and an original Pi side by side](img/a146e8640e0a448e78b4144c2b60e078.png)

The boards may be worlds apart, but the 2012 original lives on in today’s expansion connector.

Raspberry Pi 40 引脚接头和帽子形状似乎已经成为更强大的主板的事实上的标准，通常是运行 Linux 的主板。这是对来自剑桥的小板的成功的肯定，但对于 Pi 带给我们的所有好东西，我们要说扩展连接器不是其中之一。它是 2012 年 Pi 起源的受害者，来自一个当时很小的组织，生产他们认为是相对小规模的董事会，当时刚刚脱离原型状态。

第一批 Raspberry Pi 板的元件和布线选择基于权宜之计和可用资源，因此将线路引出至接头是最重要的，而不是很好地安排它们用于十年后主导该行业的大众市场板。因此，最初的 26 针接口和随后的 40 针扩展使各种接口杂乱地分布在它们周围，我们确信，如果它们今天做同样的工作，它们会给它带来一些秩序。我们喜欢使用单个 0.1”接头，但即使我们知道为什么会这样，我们也不能说引脚排列也是如此。

Feather、Pi Pico 和各种较小的 Arduinos 等双列直插式电路板具有非常方便的扩展方式，与过去的大型 DIP ICs 一样。因此，Arduino Nano 通常会安装在一块条形板上或 PCB 上，或者插在试验板上。Feather 和 Pico 则更进一步，它们都搭载了分拣附加板。我们喜欢它们的[精心设计的引脚](https://learn.adafruit.com/adafruit-feather-32u4-basic-proto/pinouts)，但我们认为单个连接器能提供更大的灵活性。

[![A BBC micro:bit and expansion board](img/564403b1ac829fad34d7a42d347d88bb.png)](https://hackaday.com/wp-content/uploads/2022/09/interface-micro-bit.jpg)

Nice board, expensive connector.

最后，我们的董事会名单中有一个采取了完全不同的策略。BBC micro:bit 是一种最初为英国学校设计的教育微控制器板，其扩展连接器是一种 PCB 边缘连接器，带有五个用于鳄鱼夹的大焊盘和 4 mm 插头，使孩子们的生活更轻松，[点缀着更精细的间距连接，带有其他接口](https://microbit.pinout.xyz/)。它的设计很好，是一个足够有吸引力的选择，它出现在相当多的竞争电路板上，但它依赖于更昂贵的专业边缘连接器插座。我们喜欢边缘连接器，但不喜欢需要昂贵连接器的连接器。

## 一切都可以变得更好

![XKCD's take on standards proliferation. (CC BY-NC 2.5) ](img/e0f76806050030039165ab3d5666e371.png)

XKCD’s take on standards proliferation. ([CC BY-NC 2.5](https://xkcd.com/927/))

因此，在调查了这个领域之后，我们有了一系列其他人已经采用的基本上是专有的标准。它们都不是 SBC 接口的完美解决方案，所以我们的下一个问题是:我们在更好的东西中会寻找什么样的品质？我们认为这个行业应该解决这个问题，但是我们认为他们应该如何解决呢？

也许最好从连接器本身开始。在这里，Raspberry Pi 采用标准的双排接头，价格便宜且易于获得，无需像 Arduino 或 DIP 格式板那样强制要求板的形状系数，也不像 micro:bit 生态系统那样需要特殊的连接器。接下来要考虑的是引脚排列。没有理由认为数字 GPIO、模拟线路和接口(如 SPI 或 I2C)不能排列在顺序编号的引脚上，以便于接口。

[![Shitty Interface, version 3.11 for Workgroups](img/29a374a6a9393363de5f8b96e8164142.png)](https://hackaday.com/wp-content/uploads/2022/09/shitty-interface.jpg)

Here’s Shitty Interface, version 3.11 for Workgroups. We defy you, nay we beg you, to do something better.

我们认为微控制器和 SoC 接口非常相似，这是可以实现的。我们也不认为制造商拥有自己的专有引脚排列有什么特别的商业优势，因为在这种情况下，排他性没有什么价值。跨多个电路板的通用引脚排列不应该像 USB 那样需要数百万美元的行业联盟，而是一组简单的 I/O 线必须连接到一组接头。

还没有发生的原因可能是没有直接的销售激励让他们这样做，但我们认为有一个角度可能证明是有说服力的。硬件制造商应该想象这样一个世界:除了所有的单板机都有相同的接口，所有的扩展卡、盾牌、帽子或翅膀也都有。突然之间，卡片的潜在市场变得更加有利可图，因为所有主要的 SBC 制造商也销售卡片，我们希望他们也能看到这种潜力。

我们很想听听我们的读者对这个问题的看法，你认为呢？