# 黑客的 m . 2–连接器

> 原文：<https://hackaday.com/2022/11/03/m-2-for-hackers-connectors/>

在第一篇 M.2 文章中，我描述了 M.2 设备的真实类型和用例，这样你在处理各种可用的卡和端口时就不会感到困惑。我自己也设计过不少 M.2 卡和收卡适配器。今天，我想告诉你你需要知道的一切，以便你自己建立 M.2 技术。

构建 M.2 有两个方面——在 PCB 上添加 M.2 插座，以及构建 M.2 卡 PCB。我将讨论这两个问题，从前者开始，知道如何处理 M.2 套接字可能是您唯一需要的东西。除了我将要描述的之外，还有一些不错的指南，你可以从中学习一些东西，比如[Sparkfun MicroMod 设计指南，](https://learn.sparkfun.com/tutorials/designing-with-micromod)其中大部分是专门针对 MicroMod 的，但也包括相当多的 M.2 技巧和窍门。

## 首先，让我们谈谈 Y 键

你能用 PCB 上的 M.2 插座做什么？首先，许多美味的业余爱好者友好的 som 和 CPU 现在都有一个 PCIe 接口，如果你正在建立一个开发板或一个简单的突破，一个 M.2 插座将让你连接一个 NVMe 固态硬盘，以满足你所有的高速低功耗存储需求——许多 Raspberry Pi 计算模块主板都有专门用于此的 M.2 M-key 插座，并且在 RPi 固件中有 [NVMe 支持](https://hackaday.com/2021/03/29/nvme-boot-finally-comes-to-the-pi-compute-module-4/)来启动。此外，你可以随时将全尺寸 PCIe 适配器或扩展器插入这样的插座，并连接 PCIe 网卡或其他急需的设备——甚至可能是，[外部 GPU！](https://hackaday.com/2022/04/28/a-real-gpu-on-the-raspberry-pi-barely/)然而，尽管配备 PCIe 的 som 很好吃，但它们远不是使用 M.2 插座的唯一理由。

PCIe 本身就是一个界面，其受欢迎程度和可访问性[都在增加。我们已经报道了有人制作了一个针对数码相机的](//twitter.com/whitequark/status/1552038782060437507)[适配器，](https://hackaday.com/2022/04/20/developing-your-own-digital-film/)让你用 NVMe 固态硬盘代替 CFExpress 卡——两个接口都以 PCIe 为主干。我们看到的一种不同的适配器可以让你[将 PCIe WiFi 卡放入 Pinebook，](https://hackaday.com/2020/04/27/adapter-brings-m-2-wifi-cards-to-the-pinebook-pro/)帮助你大幅提高 WiFi 速度。当然，不仅仅是 PCIe，即使与 SATA 或 USB 结合使用也是如此。你想在你的主板上设计一个支持 RISC-V[Linux](https://www.phoronix.com/news/Ubuntu-22.10-LicheeRV-RISC-V)的 SBC 吗？好吧，Sipeed [制造了目前可用的少数 RISC-V SOM 之一，](https://twitter.com/Sosowski/status/1481716036089139206)称为 LicheeRV，它是一个 20 美元的 SOM，使用两个 M.2 B-key 连接器，具有完全定制的引脚排列。

事实证明，你可以用一组 67 个小尺寸的管脚做很多事情。例如， [Sparkfun MicroMod](https://www.sparkfun.com/micromod) 是一个微控制器生态系统，它利用带有自定义引脚排列的 M.2 硬件——在 MicroMod 的情况下，它是 E-key 硬件，具有自定义卡长度和固定螺丝位置，这样 WiFi 卡就无法插入。对于业余爱好者来说，它们是一个整洁而有趣的生态系统，有大量不同的 CPU 和传感器可以玩——从商业角度来说，它们让我们可以评估各种不同的处理器以用于我们的应用。事实上，去年由[Thomas Flummer] 设计的 [Remoticon badge spin 是为 MicroMod CPUs 设计的，而就在最近，Hackaday Discord](https://hackaday.com/2021/11/10/the-hackaday-remoticon-2-badge-an-exercise-in-your-own-ingenuity/) 上的【tz arc】[告诉我们，他们有足够的乐趣来构建基于 MicroMod 的键盘](https://discord.gg/UfF2g7YG)[！](https://github.com/tzarc/ghoul)

我自己在 M.2 上的工作主要是改进笔记本电脑，为旧硬件注入新的活力。例如，我已经为恢复旧笔记本电脑制造了不少适配器——即小尺寸 [mPCIe 到 M.2 M-key NVMe 适配器，](https://github.com/CRImier/MyKiCad/tree/master/Laptop%20mods/mpcie_nvme)，我和我的朋友用它们将快速廉价的 NVMe 固态硬盘装入旧的但仍然可用的机器。我还为我的朋友们的用例建立了一个 M.2 键对键适配器的宝库，比如让你[用 M-key SSD](https://github.com/CRImier/MyKiCad/blob/master/Laptop%20mods/nvme_ae_to_m/) 替换 A/E WiFi 卡，或者[反之亦然，](https://github.com/CRImier/MyKiCad/blob/master/Laptop%20mods/nvme_bm_to_e/)和[苹果 Xserve 板的适配器](https://github.com/CRImier/MyKiCad/tree/master/Repairs/xserve_sata_adapter)在其专有的 SATA 引导驱动器连接器中使用 M.2 SATA SSDs。

使用 M.2 插座有很多乐趣。现在——怎么做？

## 机械指令

你加一个 M.2 插座需要什么？在机械方面，它的尺寸以及一些空闲的电路板空间。先说板空间。当然，你可以让卡挂在你的 PCB 上——把问题从“PCB 空间”转移到“机箱内的空间”区域，但你仍然需要考虑尺寸。M.2 卡的大小用 WWHH 格式的四个数字来描述，分别是以毫米为单位的宽度和高度——3042 WWAN 卡宽 30 毫米，高 42 毫米(包括卡边缘)，2280 SSD 宽 22 毫米，高 80 毫米。在 PCB 上放置封装时，与封装相关的卡边缘的确切位置要么在数据手册中明确显示，要么可以从横截面图中推断出来。

你可以买到各种各样的 M.2 插座——我将它们分为中间安装、扁平和倾斜插入，它们最重要的区别是高于你的 PCB 的高度。M.2 插座 PCB 到卡的距离实际上是标准化的，但中间安装和平面安装插座是一个不太标准化的领域——尽管如此，它们对于使您的项目变得小而薄非常有用。我非常喜欢使用扁平插座，因为它们只是将你的卡固定在适当的位置，不需要支架——也就是说，它们可能不会像一些更好的固态硬盘那样与双面卡配合使用，我也不敢在卡下放置组件。

大多数 M.2 插座，无论高度如何，都使用完全相同的 PCB 尺寸，因为它也是标准化的——除了中置插座，当您需要节省垂直空间时，中置插座非常有用，但它们的尺寸差异很大。这个尺寸实际上在规范中是标准化的，对于你遇到的绝大多数插座都是一样的。然而，一位朋友最近向我展示了情况并非总是如此—[LOTES apci 0162](https://lcsc.com/product-detail/Card-Edge-Connectors_LOTES-APCI0162-P001A_C841662.html)是一个角度插入式连接器的例子，其焊盘之间的距离比通常的封装插座更短。因此，为了以防万一，在购买新零件时一定要重新检查足迹！

## 获取和附加

像 Digikey 和 Mouser 这样合适的地方会有 M.2 连接器，按照按键、高度和安装类型很好地分类。如果你像我一样，在 LCSC 购物时选择价格而不是方便，大约一个月前，我已经[汇编了一个 LCSC 当时库存的 M.2 插座的小型数据库，](https://gist.github.com/CRImier/43406e05fdb6c857342eed8243dfb5c7)因为 LCSC 在实际跟踪重要参数方面太差了。甚至有一些 G 键插座，以防你的装置太古怪，不适合规格引脚排列！

我在 KiCad 标准库中找不到 M.2 插座封装——如果你不介意借用封装，我有一些供你重复使用。这里有 [M](https://github.com/CRImier/MyKiCad/blob/master/Laptop%20mods/mpcie_nvme/nvme_lib/Conn_TE-M.2-0.5-67P-doublesided_TypeM.kicad_mod) 、 [B](https://github.com/CRImier/MyKiCad/blob/master/Repairs/xserve_sata_adapter/Conn_TE-M.2-0.5-67P-doublesided_TypeB.kicad_mod) 和 E 键插座的足迹，这里有一个[“所有 M.2 插座垫”足迹](https://github.com/CRImier/MyKiCad/blob/master/Laptop%20mods/mpcie_nvme/nvme_lib/Conn_TE-M.2-0.5-67P-doublesided.kicad_mod)——如果你需要 G 键或其他插座足迹，拿这个并移除你不需要的引脚。同样，这也是大多数角度插入和扁平插槽适合的标准尺寸，但请检查您的特定插槽是否适合。

![](img/65233790b24818a550069d8a71ca8a44.png)

if you forget to add a standoff, you’ll have to improvise

对于有角度的插入卡，您需要一个支架–否则，在您正确按住它之前，卡不太可能机械连接。M2 硬件将发挥最佳作用，M2.5 将在紧要关头发挥作用。如果卡将被固定在你的箱子里，你可能会抓住一些螺纹插件，并完成它。然而，如果你需要将固态硬盘固定到 PCB 上，你会想要可焊接的支架——在 LCSC 购物时， [s-ol 在 Twitter 上提醒我们](https://twitter.com/S0lll0s/status/1541910633859485699),我们可以使用关键字“smtso”找到它们。

组装呢？我的经验是，你绝对会想要一个有焊膏的模板，因为这些是非常密集的 0.5 毫米间距的零件，热风枪/热板/回流炉将工作得最好。也就是说，通过足够薄的尖端和预热，你可以在电路板上刻出模板，然后在必要时使用烙铁，或者使用薄烙铁尖端的薄焊料——但如果你想组装两块或三块以上的电路板，这将是令人厌倦的。

焊接后，你可能仍然会在引脚之间留下焊桥——根据我的经验，你可以通过从下面用狭窄的热风枪喷嘴加热桥区，在桥熔化后加入焊剂，然后使用锋利的镊子或针机械分离引脚，从而漂亮地清除这些桥。如果因为你在焊盘上刷了太多的锡膏而在分离后短接，事先使用好的旧锡膏也应该有帮助。

## 电气基础

![](img/ab6c8e801011e22be5123acff3c5582b.png)

Not just any socket will do.

对于 PCIe，我建议您对固态硬盘使用 M-key，对 WWAN 兼容卡使用 B-key，对 WiFi 兼容插槽使用 E-key。这三个插槽可以分别处理多达 4 倍、2 倍和 1 倍宽的 PCIe 链路，但即使你的 CPU 上只有 1 倍 PCIe，你也可以使用这三个插槽中的任何一个，只需连接第一通道引脚——如果你想了解更多，请阅读[我们的 PCIe 黑客文章](https://hackaday.com/2021/02/03/the-bus-thats-not-a-bus-the-joys-of-hacking-pci-express/)。如果 SATA 是您想要的，那也很简单，只需要两个 diffpairs。在这种情况下，你可以使用 B-key 或 M-key，因为绝大多数 SATA 固态硬盘都是 B+M——这里是[一个我使用 M-key 进行 SATA 的主板，](https://github.com/CRImier/MyKiCad/tree/master/Laptop mods/satappy)只是因为那时我储备了一些不错的 M-key 插座。

你从哪里得到引脚和符号？首先，在 KiCad 标准库中有符号，至少在 KiCad 6 中有。除此之外，你还可以从我的回购协议中获得符号——我获得了一些用于 M 键、B 键、B+M 键、A+E 键和 E 键的符号。这些方法适用于插槽和卡，因为卡的覆盖区会忽略插槽上安装垫的缺失。如果这些是限制性的，而你需要更具体的，那么总会有不可靠的网站，以及我在上一篇文章的结尾提到的规范。

M.2 卡只需要 3.3 V，但它们可能会消耗相当多的电流。如果你正在构建定制卡，这将不是一个问题，因为你知道你的设备可能会消耗多少。然而，当在您的设计中重用现有的固态硬盘、WiFi 和 WWAN 卡时，事情可能会变得更加复杂。从笔记本电脑原理图中学习是最简单的方法-总而言之，为 WiFi 卡提供 1 A–2 A，为 WWAN 和 SSD 卡提供 1 A–3 A 可能是个好主意。此外，M.2 规范提到一些 WWAN 卡可能针对单电池锂离子范围(3 V-4.2 V)而不是 3.3 V 的输入电压构建，您可能不会遇到这种卡，它可能会写在标签或数据手册的第一页上，但了解这一点还是很好的。

![](img/cd97169a173be599dd6fd13bce38fcce.png)

An adapter tapping PCIe from proprietary Dell ODD bay and adding a SATA SSD in there while at it

PCIe 卡需要 PERST、CLKREQ 和 PEWAKE 信号。也就是说，CLKREQ 用于门控时钟以进行电源管理，并可以连接到 PCIe 主机端的 GND-作为一个证明，不断丰富的 USB 3 线滥用 PCIe 1x risers 只转发 PEWAKE 和 PERST。对于 WWAN 和 WiFi 卡上的 W_DISABLE 信号，你可能想给 VCC 增加上拉——我相信它们是低电平有效，但请仔细检查。SATA 和 NVMe 上的 DAA/DSS 信号是一种很好的“驱动活动”开漏信号，可以用来驱动 LED。SUSCLK 是一个 32 kHz 时钟，可用于卡节能，但实际上并不需要，dev SLP[是一个仅 SATA 低功耗模式](https://en.wikipedia.org/wiki/DevSlp)信号。I2C 信号可能不会有用，但如果你把它们连接到你的目标上——通过 0R 电阻，以防万一，也不会有什么坏处。

## 漂亮的细节

构建更高电流的卡，还是卡+主机组合？从技术上讲，M.2 连接器每个引脚的额定电流为 0.5 A，因此，带有 9 个 3.3 V 引脚的 M-key 的最大电流为 4.5 A，也就是说，M-key 的建议电流不超过 2.5 A，这也是您需要坚持的。如果等式的两端都在您的控制之下，并且您正在创建自己的引脚排列(最好使用 G-key 之类的东西)，那么就尽情发挥吧，尽可能多地使用不同电压的引脚。我只希望 Sipeed 知道在设计 LicheeRV 时-显然，他们[只使用一个 M.2 插座引脚](https://dl.sipeed.com/shareURL/LICHEE/D1/Lichee_RV/HDK/2_Schematic)将 5 V 电压馈入基板。我不知道这是否是一个实际的问题，但它看起来肯定不是最理想的！

![](img/a55f2fd24a5e1084736f45267d09eee6.png)面对笔记本电脑主板上不合理的非填充 M.2 插座？找到一个插座并不困难，因为封装尺寸是标准化的——尤其是如果你有原理图的话，因为那些原理图通常会列出连接器的零件号。然而，焊接连接器会更棘手，因为你不能完全把它刻在一个组装好的主板上。我建议您首先吸掉工厂应用的焊料，以便连接器可以与 PCB 齐平，然后将连接器放上，并使用薄烙铁和薄焊料逐个连接焊盘。从那以后，一些电源管理器件和信号无源器件，比如说电容，可能就没人用了。PCIe 或 SATA 系列电容的合适值[约为 220nF](https://electronics.stackexchange.com/questions/632972/can-i-use-a-250-nf-instead-of-a-200-nf-smd-ceramic-capacitor) USB 信号和 PEWAKE/CLKREQ/PERST 之类的东西可以与 0R 或 22 R 之类的东西跳线，电源管理通常可以直接跳线到 3.3 V，其他许多信号你会发现是可选的。

现在，你已经准备好构建和破解接受 M.2 的东西，并且知道它在相当多的地方有用。下一次，我将向你展示如何制作 M.2 卡片——这些卡片也有很多很酷的应用！