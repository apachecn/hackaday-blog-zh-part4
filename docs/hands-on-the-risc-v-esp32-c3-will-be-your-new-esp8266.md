# 动手操作:RISC-V ESP32-C3 将是您的新 ESP8266

> 原文：<https://hackaday.com/2021/02/08/hands-on-the-risc-v-esp32-c3-will-be-your-new-esp8266/>

我们刚刚拿到了一些 [ESP32-C3 芯片和模块](https://www.espressif.com/en/products/socs/esp32-c3)的工程预样品，这款芯片有很多令人喜欢的地方。问题是你应该拿这个和什么比较；更像是 ESP32 还是 ESP8266？新的“C3”版本具有一个 160 MHz RISC-V 内核，性能优于 ESP8266，同时包括 ESP32 的大部分外围设备。虽然 RAM 在大约 40 kB 的 ESP8266 上经常变得稀缺，但 ESP32-C3 拥有 400 kB 的 RAM，并设法在消耗更少功率的同时保持全部运行。和 ESP32 一样，它除了 WiFi 之外，还有蓝牙 LE 5.0。

Espressif 的网站多次表示这将是“划算的”，这是廉价的秘密代码。有传言称，将有 8 针 ESP-O1 模块上市，价格低至 1 美元。我们通常需要更多的引脚，但如果中型 ESP32-C3 模块的价格接近 ESP8266-12 型模块，我们看不出有任何理由购买后者；对我们来说，这简直就是一个 ESP8266 杀手。

另一方面，它缺少 ESP32 的双核，也没有那么多 GPIO 引脚。如果你是一个顽固的 ESP32 滥用者，你无疑会发现一些功能缺失，如超低功耗协处理器或 DAC。但是*和*有很多 ESP32 的突出之处:LEDC (PWM)外设和独特的并行 I2S 浮现在脑海中。此外，它与 ESP32 共享 [ESP-IDF](https://github.com/espressif/esp-idf) 框架，因此尽管运行在完全不同的 CPU 架构上，但只要通过一行代码调整构建环境，许多代码就可以在两个芯片上运行而无需更改。

[![](img/d2de595e06d364c2998573b23afc8608.png)](https://hackaday.com/wp-content/uploads/2021/02/DSCF2253_thumbnail.png)

One of these things is not like the other

如果你像我们一样对芯片的名字感到困惑，玩一周左右的新芯片会让你明白一切。ESP32-C3 更像是 ESP32 的缩小版，而不是 ESP8266 的改进版，尽管它可能注定要在我们的项目中扮演后者的角色。如果算上带 USB 接口的[新 ESP32-S3](https://github.com/espressif/esp-idf) ，ESP32 家族不仅仅是一个芯片。虽然将 RISC-V 和 Tensilica CPUs 放在一起*看起来有点奇怪，但归根结底，区分微控制器的是外设而不是 CPU，在这方面，C3 是 ESP32 家族的一员。*

我们的收获:在我们的项目中，ESP32-C3 将取代 ESP8266，但它不会取代 ESP32，因为它只是在我们需要时提供更多功能。当我们不需要成熟的 ESP32 时，共享的代码库和外围架构使两者之间的切换更加容易。本着这种精神，我们欢迎家庭的新成员。

但是自然地，我们有更多的话要说。具体来说，我们对 RISC-V 内核到底带来了什么感兴趣，并通过与 ESP32 和 ESP8266 的功率和速度比较来运行该模块，在我们的基准测试中，它以微弱优势击败了它们。我们还与所有 ESP32 系列芯片都使用的 ESP-IDF SDK 成为了非常亲密的朋友，并且非常喜欢它在过去一年左右的时间里取得的进步。当然，它不像 ESP-Arduino 那样对新手友好，但它的功能更强大，我们非常高兴将 ESP8266 SDK 抛在身后。

## RISC-V:功率和速度

ESP32-C3 与 ESP32 和一些外设共享编码框架，并且具有大约相同的内存量。有什么不同？C3 的 RISC-V CPU 与 ESP32 和 ESP8266 中的 Tensilica 内核。所以我们想测试一下它们的速度，看看它们在处理速度和整体功耗方面的表现如何。

[![](img/049a59a1c51a678bcc6b4efb4ed8a29d.png)](https://hackaday.com/wp-content/uploads/2021/02/DSCF2244_thumbnail.png) 就微控制器和其他嵌入式设备的标准基准而言， [CoreMark](https://www.eembc.org/coremark/) 可能是首选。我们发现它已经被[Ochrin]移植到了 ESP8266 和 ESP32 上。(谢谢！)CoreMark 包括三个测试:用链表查找和排序以加重内存单元的负担，运行状态机以测试 switch/case 分支速度，以及矩阵乘法任务以加重 CPU 和编译器的负担。

在实践中，模仿我们使用 ESP8266 和 ESP32 框架的一般经验，针对 ESP32 和 ESP32-C3 编译的代码没有任何麻烦。相比之下，让它在 ESP8266 上运行是非常麻烦的，花了几个小时来降低 RTOS 框架的版本，在 Python 2 中安装模块`virtualenv` s，并获得一组`PATH` s 和其他环境变量*恰到好处*。但是我们不能丢下你不管，所以我们开夜车。

[![](img/4d6b51794c48cf778623150903b1aa8a.png)](https://hackaday.com/wp-content/uploads/2021/02/coremark-1_reformatted.png)

要点是，ESP32-C3 上的单个 RISC-V 内核的每 MHz 速度比基于 Tensilica 的设备上的单个内核稍快。当然，如果你正在努力处理数字，并且使用了 ESP32 的两个内核，那就完全不同了，你知道你是谁。但是，如果你在 ESP32 上运行 Arduino，并且你自己没有[明确地运行 RTOS 任务](https://randomnerdtutorials.com/esp32-dual-core-arduino-ide/)，或者运行 MicroPython 而不使用线程，你可能在 ESP32 上运行单个内核。模一些小的差异，有一个免费的核心来专门处理 WiFi，你可能不会比 C3 差太多。

[![](img/ef84aebeed4a75241cd442181839eb76.png)](https://hackaday.com/wp-content/uploads/2021/02/DSCF2263_thumbnail.png) 在进行这项测试时，我们还将我们超级复杂的功率测量单元连接到被测设备上，一根带有三个 3ω电阻的 USB 电缆和一个示波器。当然，如果你只是想要芯片的功率规格，你可以点击数据表。

相反，我们在这里看三个不同模块的真实性能:用于 ESP8266 的 WeMos D1 迷你，用于 ESP32 的 Lolin 32，以及我们的演示 ESP32-C3-DevKitC-1，直接来自 Espressif。所有都是在 led 关闭的情况下运行，或者在 ESP32-C3 装置的情况下用侧切割器简单地修剪。(这并没有太大的区别，但你不试试就不会知道。)

利用功耗数据，我们还可以检查模块的能效，以每毫瓦的 CoreMark 分数衡量。在这里，ESP32-C3 做得比 ESP8266 好一点，介于分别运行一个内核和两个内核的 ESP32 之间。这证实了我们一段时间以来的怀疑——如果你想省电，最好的办法是让芯片尽可能多地休眠，然后在需要运行时全力运行。如果您使用的是 ESP32，请使用两个内核。

[![](img/27b52e27ef06bb457e2bcfdcbd54a3cf.png)](https://hackaday.com/wp-content/uploads/2021/02/coremark_efficiency-1_reformatted.png)

虽然我们的结果*在功率和速度方面绝对意义重大且可重复，但它们并没有改变游戏规则。如果我们真的需要粉碎浮点，我们会选择更适合这项任务的芯片，如 STM32F4xx 或 STM32F7xx，或者 Teensy 4.0 中的恩智浦/飞思卡尔 600 MHz i.MX ARM7 芯片[。如果你买了一个 ESP-任何东西，那是因为你想要无线连接，很高兴知道你没有放弃任何关于 CPU 速度的 ESP32-C3。](https://hackaday.com/2019/08/07/new-teensy-4-0-blows-away-benchmarks-implements-self-recovery-returns-to-smaller-form/)*

我们在介绍中暗示过，但这种芯片的 RISC-V 性质，至少在用户体验方面，是*没什么大不了的*。您可以像使用任何其他工具链一样进行编码、编译和刷新。ESP-IDF 使使用新芯片变得简单，只需输入`idf.py set-target esp32c3`和`idf.py fullclean`即可。然后你去忙你的事。在这个测试过程中，我必须交换 30 次架构，事实上就是这么简单。

## 外围设备和引脚

ESP8266 遇到的第一个限制是它没有足够的 GPIOs 或 ADC 来支持您的特定项目。虽然 ESP32 在纯粹的 GPIO 数量上是一个重大改进，但一旦你考虑到具有专用功能的引脚或仅作为输入的引脚，你就可以轻松地突破芯片的极限。因此，你可以设计一个外部 ADC 芯片，并通过 I2C 连接它，或者你可以添加一个移位寄存器，并用速度极快的 I2S 外设来驱动它——这是 ESP8266 无法做到的。

与 ESP32 共享外设集将有助于缓解 ESP32-C3 的一些问题，即使它与 ESP8266 具有相同的引脚数。见鬼，如果你愿意分配他们，C3 甚至有 JTAG 的能力。而 JTAG 不是，许多硬件外设可以分配给你想要的任何引脚。

但是我们不得不得出结论，用 ESP32-C3 设计仍然很像为 ESP8266 设计。I/O 受限。你必须接受这个事实。

## 定位 ESP-C3

ESP8266 最初是一个简单的 AT 命令集 WiFi 调制解调器，一群黑客[证明它可以提供更多](https://hackaday.com/2014/11/23/using-the-esp8266-as-a-web-enabled-sensor/)。有时很难记起在 ESP8266 之前 WiFi 连接有多困难和昂贵，但在当时，5 美元的 WiFi 与 50-100 美元的 [WiFi 相比是革命性的。一晃几年过去了，ESP32 本身就是一款有能力的微控制器，带有](https://en.wikipedia.org/wiki/Linksys_WRT54G_series)[一些很酷的古怪功能](https://hackaday.com/2016/09/15/esp32-hands-on-awesome-promise/)。哦，对了，还有无线网络和 BLE。我们在很短的时间内走了很长的路。

[![](img/6bf1c4b575308ba313c0401efecf7cb7.png)](https://hackaday.com/wp-content/uploads/2021/02/DSCF2233_thumbnail.png)C3 实际上是两者的融合:像 ESP8266 一样的有限数量的 GPIO 引脚，但有像 ESP32 这样的漂亮外设。如果它的定价与 ESP8266 竞争，它将推动该芯片退役。但也许是时候了。

ESP-IDF 已经在我们身上成长起来，但与 ESP-Arduino 的过多例子或 MicroPython 难以置信的易用性相比，它仍然微不足道。当后者移植到 ESP32-C3 上时，其内存比 ESP8266 显著扩展，这将是一个非常便宜的平台，会使许多人放弃再次编译。但是，当您需要原生 SDK 的速度时，能够依靠现有的 ESP32 代码库是很好的，所以穿着 ESP32 服装的 ESP8266 是赢家。

我们已经获得了预生产样品，Espressif 仍在 IDF 中致力于支持 ESP32-C3 的所有功能。见鬼，反正你也买不到 ESP32-C3 模块，所以我们只能盯着我们的水晶球看一会儿。但是关于类似于 ESP8266 的定价的杂音让我们注意到了这一点，如果市场能够承受的话，即使价格溢价很小，这也是一次值得的升级。与此同时，ESP32-C3 从根本上来说不如 ESP32，所以它的价格应该更低。ESP8266 开发板售价为 2 美元，ESP32 开发板售价为 4 美元，这没有留下太多的回旋余地，我们怀疑一些人会为 ESP32 买单。所以很难说价格到底有多重要。

但是很高兴在更多的设备中看到 RISC-V 内核，尤其是因为标准化指令集架构——本质上相当于一组标准的机器语言命令——使编写优化编译器变得更容易、更快。对于最终用户来说，这并不重要，但如果节省 IP 许可费可以让 Espressif 以 ESP8266 的价格包含更现代的外设集，那么我们都支持它。