# 连接器动物园:I2C 生态系统

> 原文：<https://hackaday.com/2022/05/04/the-connector-zoo-i2c-ecosystems/>

I2C 是一个很棒的界面。只需四根线和两个 GPIOs，您就可以连接大量的传感器和设备——并行连接！你会发现 I2C 几乎无处不在，用在每一部手机、笔记本电脑、台式机以及任何内置多个 IC 的设备上——而且大多数微控制器的硬件中都内置了 I2C 支持。因此，有无数有趣和有用的设备可以配合 I2C 使用。偶尔，面向制造商的公司为他们生产的 I2C 设备分线点创建即插即用接口，具有标准化的引脚和连接器。

遵循一个标准的引出线比发明你自己的要好得多，你在来自中国的通用 I2C 模块上不一致的管脚引线的经历肯定会反映出这一点。如果您可以将一个带有 I2C 的连接器插入您花几美元购买的 MPU9050、MLX90614 或 HMC5883L 分线点，而不是像通常那样查看模块的丝网印刷、将引脚接头焊接到其上并仔细将母接头排列到正确的引脚上，这不是很好吗？

与任何标准一样，当涉及到连接器上的 I2C 约定时，您会正确地猜到不止一个，并且它们都有各自的优缺点。不太有[十五](https://xkcd.com/927/)，但绝对有六个半！它们大多是相互兼容的，利用它们意味着你可以很容易地访问一些非常强大的外设。让我们从两个只有细微差别的生态系统开始，这两个生态系统是你会遇到最多的！

# JST-SH 的伙伴们

![QWIIC and STEMMA QT JST-SH footprint and symbol](img/851ef8bead27e17ddc0efdb3f87aa00b.png)

KiCad symbol: Conn_01x04_MountingPin; footprint: JST_SH_SM04B-SRSS-TB_1x04-1MP_P1.00mm_Horizontal

I2C 模块有两种生态系统，它们基于四针 JST-SH(1 毫米间距)连接器，并且非常容易互换！其中一个是 Sparkfun 的 QWIIC，另一个是 Adafruit 的 STEMMA QT(发音为‘cutie’)。只要准备好几个 JST-SH 四引脚连接器，它们都可以直接添加到 PCB 中。此外，Adafruit 和 Sparkfun 连接器具有相同的引脚排列！

使用的连接器是 JST-SH，表面贴装，间距 1 mm。他们的 JST 系列是 SR/SH，原始 JST 零件的零件号是 [SM04B-SRSS-TB](https://www.digikey.com/en/products/detail/jst-sales-america-inc/SM04B-SRSS-TB/759911) ，但你可以在 LCSC 上使用“1x4P SH 1mm”搜索词找到相同尺寸的廉价第三方连接器。在做自己的设计时， [QWIIC](https://www.sparkfun.com/qwiic#faqs) 和 [STEMMA](https://learn.adafruit.com/introducing-adafruit-stemma-qt/technical-specs) 都有可以参考的页面。那么，这两者有什么区别呢？

QWIIC 将主机(即 MCU 板，提供电源)和设备(即传感器，消耗电源)端的电压限制在 3.3 V，这是一个合理的决定，大大简化了工作。如今，我们使用的绝大多数器件都是 3.3 V，电平转换问题几乎闻所未闻。也许，最终迁移到 1.8 V 会改变这种情况，但我们还没有达到这一步，无论如何，当我们达到这一步时，LED 正向电压等因素将使我们的项目中需要某种高于 1.8 V 的基准电压源。因此，一个连接器上有 3.3 V 电源和两个 3.3 V 逻辑电平 I2C 信号——简单明了。很有可能，您已经可以将 QWIIC 添加到您的传感器或 MCU 板上，除了连接器本身，不需要任何其他组件！

![STEMMA QT sensor with a cable plugged into it](img/5f778ef39cfbb03ede029b73f4f24703.png)

STEMMA QT sensor; photo by Adafruit

相比之下， [STEMMA QT](https://learn.adafruit.com/introducing-adafruit-stemma-qt/what-is-stemma-qt) 旨在扩展可能的教育和便利价值，与其他 Adafruit 产品保持一致。因此，它允许 5 V 主机——设备[设计为在 3.3 V-5 V 电源和逻辑电平范围内工作，](https://learn.adafruit.com/assets/110406)确保你的 Arduino Uno 不会被排除在游戏之外。这是可能的，因为每个模块都有一个低压差稳压器，如 AP2112K 或 MIC5219，当你向电路板提供 3.3 V 电压时，它有助于保持大约-3.3 V。原因很简单——除了 Arduino Uno 等 5 V 主机，你可能还想用一些耗电设备链接 STEMMA 设备，如 I2C 伺服系统或 RGB 条。简而言之，用任何种类的链条将任何东西插入任何东西，都不应该导致神奇的烟雾逸出——这种事件很少出现在制造商项目的待办事项列表中。STEMMA QT 的另一个优势是设备板尺寸的标准化，让您可以在新传感器到达您面前之前轻松地将其机械集成到项目中，并催生出一些漂亮的黑客，如[这款 STEMMA Qt 3D-printable hotswap 插座！](https://hackaday.com/2022/04/04/quick-swap-socket-for-stemma-qt-experiments/)

总结一下电压兼容情况——所有 STEMMA QT 设备都将与 QWIIC 主机一起工作；并且所有 QWIIC 设备都将与 3.3 V STEMMA Qt 主机一起工作；因此，任何 QWIIC 主机在技术上也是 STEMMA QT 主机。QWIIC 设备将与 5 V STEMMA QT 主机严重不兼容，但这种主机很少，当 QWIIC 设备与 STEMMA 主机接口时，您只需保持警惕。这两种标准的另一个小问题是缺乏中断信号——我将在下面的“突破花园”一节中详述。暂且先来看看 STEMMA QT 的大姐姐吧！

## 链接 QWIIC 和 STEMMA 模块

![Three rotary encoders from STEMMA QT ecosystem being chained](img/23f3245bab3a8a0a1602243616c973cc.png)

Three I2C QT Rotary Encoders chained; photo by Adafruit

哦，对了，连锁！QWIIC 和 STEMMA QT 都是链友好型的，许多模块在电路板的另一侧提供第二个 JST-SH 连接器，传递相同的信号。这使您能够以一种舒适的方式连接您的项目，而不必在项目中找到一个可以放置 MCU 的位置，同时不要让它离所有传感器太远，或者不要求助于试验板来将 I2C 总线分成多个短线。许多主板还提供多个并行连接的插座，还有“分离器”板可以将一根带 I2C 的 JST-SH 电缆变成三个额外的插座。

只要你的地址不冲突，你通常可以用这种方式为一个项目在 I2C 总线上布线。哦，确保[不要让你的 I2C 总线](https://hackaday.com/2016/07/19/what-could-go-wrong-i2c-edition/)过载，因为所有上拉电阻都是并联的 STEMMA QT 的上拉电阻往往是 10kω，QWIIC 的上拉电阻往往是 2.2kω，至少在 QWIIC 的情况下，你通常可以用 xacto 刀切断两个走线跳线，以断开任何模块上的上拉电阻。由于所有非 Pico 型 Raspberry Pi 板的 I2C 端口上都有 1.8kω板载上拉电阻，您可能会发现自己需要在链接器件时尽早这样做。

# 更大、更黑的连接器

![STEMMA footprint and symbol](img/ce00d7736bae6df729c3f76ff6b7aabb.png)

KiCad symbol: Conn_01x04_MountingPin; footprint: JST_PH_S4B-PH-SM4-TB_1x04-1MP_P2.00mm_Horizontal

[STEMMA](https://learn.adafruit.com/introducing-adafruit-stemma-qt) 的引脚排列与 STEMMA QT 和 QWIIC 相同，但连接器不同，且更大。当涉及到可以在主机端输出的电压时，它也是灵活的，并且反过来，必须能够在设备端接受。STEMMA QT 部分的大部分优势适用于 STEMMA，除了 QWIIC 兼容性和物理尺寸减小。

STEMMA 连接器是间距为 2 mm 的 JST PH 连接器，JST 零件号为 [S4B-PH-SM4-TB](https://www.digikey.com/en/products/detail/jst-sales-america-inc/S4B-PH-SM4-TB-LF-SN/926657) ，有“1x4P PH 2mm”搜索词的廉价第三方连接器。它们比 1 毫米间距的 SH 连接器更容易用烙铁处理，对于[更大的电路板](https://www.adafruit.com/product/4026)，它们是一个很好的选择。

JST-PH 是表面贴装插座比通孔插座更有弹性的例子之一。有了更坚固的保持机制，你的指甲将不再足够——你可能会想用你信赖的蓝色平头剪来拔掉它们！携带 I2C 的 STEMMA 也有一个 GPIO 和模拟 STEMMA 对应产品，使用 3 引脚 JST PH 连接器，用于 WS2812 条之类的东西——其中 5 V 兼容性变得非常方便。然而，4 针连接器坚定地为 I2C 保留，这种一致性在教育和原型开发环境中很难不受到重视——查看[几十个教程](https://learn.adafruit.com/category/stemma) Adafruit 涉及 STEMMA 设备，其中的“布线”部分非常简单！在一些 STEMMA 主机上，你也可以通过一个跳线[将端口](https://cdn-shop.adafruit.com/970x728/4116-15.jpg)重新连接到 3.3 V 或 5 V。

# 就是进不了小树林

![Grove connector on some digital microphone breakout](img/f111c85acea7229e1cf2728245e6af72.png)[格罗夫连接器标准](https://wiki.seeedstudio.com/Grove_System/)，他们中最古老的，现在有点像 I2C 连接器生态系统中的害群之马，这里一半是一段历史，一半是一个警示故事。与开源生态系统的原则相反，Grove 使用了一种专有的连接器，这种连接器[让制造商争夺其正确的标识](https://arduino.stackexchange.com/questions/9030/what-type-of-connector-does-the-grove-system-use)，因为他们试图找到一个不被视为 Studio 的资源。与这里列出的所有其他标准不同，当你看到 4 针 Grove 连接器时，你不知道它是用于 I2C、UART、两个数字 GPIOs 还是模拟的，这破坏了整个“即插即用”的想法。

对于那些不幸不得不与 Grove 接口的人来说，它也使用 3.3v-5v 范围的可能电压，但对明确宣传使用哪一种电压不太感兴趣，或者让你改变这一点-这两件事 STEMMA 都不费吹灰之力。它使用与 QWIIC/STEMMA do 相同的 I2C 引脚排列。如果您有兼容 STEMMA(JST-PH)的电缆，您可以稍微打磨一下，使其适合 Grove 连接器。

换句话说，有一个很好的理由让你看不到更常用的 Grove 连接器。我不禁注意到，在撰写他们自己的 [I2C 连接器生态系统概述文章](https://www.tomshardware.com/features/stemma-vs-qwiic-vs-grove-connectors)的结论部分时，Tom's Hardware 未能发现 Grove 的一个优势，而这一优势在他们谈到的其他生态系统中并不普遍。除非你愿意为你需要的每一个连接器和电缆支付 SeeedStudio，并且不介意与值得投入精力的连接器生态系统兼容，否则我强烈建议你不要在主板上使用 Grove。让我们把时间花在下一个不受重视的选项上。

# 在突破花园中漫步

!["Breakout Garden" footprint and symbol](img/6bcf3675703743ebc4f1348654a7b67b.png)

KiCad symbol: Conn_01x05; footprint: PinHeader_1x05_P2.54mm_Vertical

[Pimoroni 的 Breakout Garden 生态系统](https://shop.pimoroni.com/collections/breakout-garden)采用了优雅的引脚排列——从 [Raspberry Pi GPIO 头](https://pinout.xyz/pinout/i2c#)上取下一排五个引脚，引脚 1 至 9，包括 3.3 V、SDA、SCL、一个 GPIO 引脚，当然还有 GND——按此顺序排列。他们肯定没有这种引脚排列的专利——很多黑客，包括我自己，已经在我们配备 I2C 的主板上使用这种引脚排列很多年了。首先，这种引脚排列意味着你可以直接将任何分线板插在树莓派上。

你也不限于此——Pimoroni 还提供了漂亮的滑入式连接器，让你可以热插拔突破花园模块。此外，如果您不想使用滑入式插座，只需焊接成角度的公插头，并像对待任何其他模块一样对待它们。分线花园模块的输入电压范围通常为 3.3 V 至 5 V。他们还声称每个模块都有反极性保护，因此，不可避免地将一个模块向后插不会延误您的项目。

利用分线花园引脚排列，您还可以获得一个额外的 GPIO，它通常是 NC 或用作中断引脚。当与 I2C 设备一起工作时，中断引脚被低估了——它们让你卸载你的 CPU 和你的 I2C 总线，避免轮询，并让你的 I2C 外设在它需要你的注意时向你发出信号，这仅仅通过 I2C 总线是不可能的。对于一些模块，如[这个触觉致动器驱动器](https://shop.pimoroni.com/products/drv2605l-linear-actuator-haptic-breakout)，GPIO 被用作“触发”引脚，用于动作同步。当然，这确实在一定程度上损害了链接的概念——公平地说，庞大的 hotswap 套接字也是如此。这并不是说你不能并行连接分支花园板——毕竟，INT 引脚通常对于 I2C 设备是禁用的，这绝对会派上用场，考虑到将所有 INT 引脚连接在他们的[6-socket Raspberry Pi HAT](https://shop.pimoroni.com/products/breakout-garden-hat)上的令人困惑的决定。

在您的项目中添加对“突破花园”式连接的基本支持就像添加一个 5 引脚 2.54 毫米(0.1 英寸)引脚接头一样简单，这样，您就可以立即获得 Raspberry Pi GPIO 接头兼容性。当谈到创建自己的模块时，我找不到任何维度或官方的“如何创建”模块，所以你可能不打算这样做-这并不意味着你不能逆向工程原理图和维度，然后尝试，但它肯定是相当令人沮丧的。如果你想添加一个花园插座，它们有两排相距 5.08 毫米(0.2 英寸)的插脚，并提供方便的插头连接，尽管每个插座的成本为 1 英镑(不包括运费)，滑入式插座是所有插座中最贵的。

# 方便卷曲的电缆

![Picture of a miswired JST-SH 4-pin cable. On one end, red wire is wired to pin 1, but on the other end, it's wired to pin 4 - and so on.](img/22155a383c28a7f5dbaadc400a1a647a.png)在市场上寻找一些 JST-SH 配件？你真的不能出错的 SMD 连接器；然而，当涉及到预压接电缆时，你绝对会出错。压接间距为 1 毫米的 JST-SH 绝非易事，购买自己的电缆是最好的选择——除非它们接线错误。一年前，我正在为一个项目做准备，买了一捆 JST-SH 电缆，如右图所示。经过仔细检查，感觉有些不对劲。

结果发现，他们的电缆末端接线方向相反，一个的引脚排列与另一个相反——当用作互连时，可能会产生灾难性的后果。我买的电缆需要用镊子小心地重新布线，下次你在购买第三方 JST-SH 电缆以便为下一个项目布线时，你会知道在按下“立即购买”按钮之前检查图片。

# 提及可变荣誉

![Some DFRobot module, with a JST-PH connector, miswired compared to STEMMA/QWIIC as described in the article](img/0af2003e830da3d79c9fc30815c2943a.png)如果你曾经使用过 DFRobot 零件，你可能也在它们的电路板上见过 JST-PH 4 针(或 3 针)连接器——它们来自他们的[生态系统，名为重力](https://www.dfrobot.com/gravity.html)。令人费解的是， [Adafruit 声称](https://learn.adafruit.com/introducing-adafruit-stemma-qt/dfrobot-gravity)STEMMA 与 Gravity 兼容，除了他们的非 I2C 设备——因为 Gravity 与 Grove 做同样的事情，在 Grove 中，4 针连接器不能保证 I2C。然而，[检查重力 I2C 设备的引脚排列](https://wiki.dfrobot.com/Gravity:%20I2C%20Digital%20Wattmeter%20SKU:%20SEN0291#target_4)，似乎每个引脚都在不同的位置，特别是接地和电源被颠倒。就像 STEMMA 一样，他们使用 [3 针连接器](https://www.dfrobot.com/product-798.html)用于数字和模拟设备。有趣的是，他们还设法[在某些时候改变了那些](https://image.dfrobot.com/image/data/SEN0127/pin%20mapping%20comparison.jpg)的引脚排列，*也反转了电源引脚的极性—*同时仍然使用相同的连接器，这是连接器标准的禁忌。小心行事！

[EasyC](https://e-radionica.com/en/easyc) 基本上是 QWIIC 复制到一个 T，具有相同的引脚排列、连接器、链接能力和 3.3 V 电压限制——但在他们的网页和资源中没有以任何方式提到 QWIIC，这令人失望。不同生态系统的互操作性是它们有价值的一部分，可以说，如果你知道他们使用的标准是一个被广泛接受的标准，你可能会更倾向于从他们那里购买，而不是“在一些连接器上随机引出线”。EasyC 由一家总部位于克罗地亚的 e-radionica 公司驱动，以欧洲价格生产中等规模的有用模块，包括相当多的中国模块克隆和混音。他们模块的设计文件没有链接到产品文件，但是至少他们中的一些看起来是在 GitHub 上的[!](https://github.com/e-radionicacom)有趣的是，他们还为[储备了一根 5 厘米长的“EasyC”电缆](https://e-radionica.com/en/easyc-cable-5cm.html)，经过仔细检查，这根电缆与我在上一节中提到的电缆有着相同的反向接线。或许，在 EasyC 生态系统上投入更多的思考是有必要的。

有时，我们看到一些公司在尝试 JST-SH，但并没有完全实现。这方面的一个例子是 Lolin 最近推出的电路板，Lolin D1 迷你 Pro，上面有一个 JST-SH 4 针连接器，标有“I2C”。你可以原谅[认为这是一个类似 QWIIC 的引脚排列；](https://www.reddit.com/r/arduino/comments/gc01ld/is_the_i2c_connector_on_the_lolin_d1_mini_pro/)鉴于这个接头标有“I2C”，人们可以说他们被耍了，被暗算了，很有可能是被骗了。该板使用 GND-SDA-SCL-VCC 引脚排列，而不是 GND-VCC-SDA-SCL 引脚排列，似乎甚至有一些配件，如屏蔽就是根据这种引脚排列制作的。这就好像有人给 Lolin 写了一封信，说“嘿，你应该把 I2C 放在 JST-SH 连接器上”，然后拒绝进一步详细说明。谢天谢地，有了 GND 别针的配合，毁坏东西的可能性就不那么大了。

# 建造你自己的东西？需要指导？

设计自己的主板时，应该遵循哪一个标准？我已经为你提供了你自己做决定所需要的所有信息，但是如果你在寻找建议或指导方针，我也很乐意提供。

我个人不使用全尺寸的 STEMMA (JST-PH)连接器，因为它们往往体积庞大，足以使 PCB 本身看起来很小，并且由于它们的高度，可能会使小电路板有点笨重——另外，它们可能更难拔出。然而，JST-SH 连接器太诱人了，因为只要我不使用 5V 主机，它就可以同时兼容两种生态系统。此外，一个简单的标准 5 引脚排线接头提供了惊人的好处，让您可以快速添加它！

![The proposed solution for I2C connectors on boards - a JST-SH QWIIC-like connector next to a 5-pin pin header connector, with schematics shown.](img/a429bf6614ca0b04fcd9c889f2c63db8.png)

简而言之，我建议您在您的主板上组合一个花园式引脚接头和 QWIIC/STEMMA QT JST-SH 连接器。通过这种方式，您将始终与值得讨论的四个生态系统中的三个保持兼容，并且将您的 I2C 板连接到 Raspberry Pi 将像获得五根跳线一样简单。有了这种组合，你再也不用考虑 I2C 接头引脚排列了，当你真正需要使用时，你会有一个方便的中断信号。

一定要加电平转换吗？如果您的项目中不使用 5 V，尤其是如果您要突破具有宽输入电压范围的 IC，比如 I2C EEPROM 和 RTC，就更不可能了。我个人主要使用 3.3 V 电压，我没有将 AP2112 稳压器卷轴撒在我制作的每个电路板上——谢天谢地，我也没有 5V I2C 主机。如果您确实想让您的设备兼容 5 V，那么经典、优雅且廉价的[MOSFET I2C 电平转换解决方案绝对不会错！](https://learn.adafruit.com/introducing-adafruit-stemma-qt/technical-specs#data-lines-3035228-6)

# 结论

其中，QWIIC、STEMMA 和 Breakout Garden 经受住了时间的考验，业余电子公司一直支持它们。我们从他们创造的标准中受益才是公平的。希望所提供的见解和说明让我们更接近通用互操作性时代，那时一个黑客的 MCU 板可以与其他黑客的传感器无缝对接。从那里开始，有一天，我们最喜欢的 SSD1306 有机发光二极管突破可能会开始进入我们配备 JST-SH 连接器和额外电缆的邮箱。今天还不是那一天，但是随着我们在 PCB 上添加的每一个 JST-SH 足迹，我相信我们很快就会看到它。