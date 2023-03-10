# NFC 性能:一切尽在天线

> 原文：<https://hackaday.com/2021/11/10/nfc-performance-its-all-in-the-antenna/>

NFC 标签是实验的常见目标，无论是简单地通过使用手机上的应用程序来询问或写入标签，还是通过现成的模块将标签纳入项目，或者从头开始使用标签设计项目。然而，它们并不总是容易做对，而且经常会给出令人失望的结果。本文将试图揭开 NFC 项目性能不佳的最可能原因，即读卡器本身的拾波线圈天线。

[![A selection of the NFC tags on my desk](img/3e023c1fe2c50fded39f28cfe2a49013.png)](https://hackaday.com/wp-content/uploads/2021/10/nfc-pile.jpg)

A selection of the NFC tags on my desk

这些标签包含通过射频场供电的芯片，射频场为它们提供足够的能量来启动，在这一点上，它们可以与主机进行通信，无论它们的目的是什么。

“NFC”代表“近场通信”，其中数据可以在物理上邻近的设备之间交换，而无需物理连接。读取器和标签都通过天线来实现这一点，天线采用扁平线圈和电容器的形式，共同构成谐振调谐电路。读取器发出射频脉冲，一旦从卡接收到应答就保持该脉冲，因此可以建立通信，直到卡离开读取器的范围。

## 很少有 NFC 标签和读取器在同一频率上

对于大多数可能被黑客阅读器试验的标签，RF 频率是 13.56 MHz，并且 RF 发射应该在磁场平面而不是电场中。天线并不复杂，事实上，通过缠绕合适的线圈并用一个小的可变电容器调谐，自己制作一个天线非常容易。天线的射频特性可以用信号发生器和示波器这样简单的仪器来研究，或者如果你是一个足够老的无线电爱好者，可以用倾角仪来研究。出于本文的目的，我使用 NanoVNA，因为它非常方便，我将它设置为测量端口 1 上的 SWR，扫描范围为 10 MHz 至 20 MHz。我通过 RF 拾波线圈将它松散地耦合到我正在测试的 NFC 天线，一圈直径约 10 毫米的导线焊接到同轴连接器上，并用一点胶水固定。当我将拾波线圈放在 NFC 标签上时，我得到的奖励是 VNA 上的一个尖峰，从无限远到接近 1:1 的 SWR。这适用于大多数读卡器线圈和仅包含一个存储芯片的低功耗 NFC 标签，但我的 VNA 无法提供足够的能量来测量具有更高功率集成电路的标签，如银行卡、公共交通卡或我的护照。

 [![My quick RF pickup coil](img/735add515ad66b7e204a6d31fb8b6712.png "nfc-pickup")](https://hackaday.com/2021/11/10/nfc-performance-its-all-in-the-antenna/nfc-pickup/) My quick RF pickup coil [![The VNA shows a clear SWR dip for an NFC tag](img/70ffbfbe9fe1d7372d4da85b14ed50a9.png "nfc-VNA")](https://hackaday.com/2021/11/10/nfc-performance-its-all-in-the-antenna/nfc-vna-2/) The VNA shows a clear SWR dip for an NFC tag

VNA 立即指出了大量生产的 NFC 固有的问题之一，即谐振频率很少精确到 13.56 MHz。在写这篇文章时，我发现卡和读卡器似乎都在 13.5 到 15 MHz 之间的任何地方产生共振，大多数是在 14 MHz 左右测得的。实际上，大多数读取器提供的能量都绰绰有余，因此尽管导致效率低下，标签仍然可以通电，但对于任何以最大效率工作的 NFC 标签系统来说，它应该将读取器和标签都调整为在 13.56MHz 的通信频率下谐振。

## 银行卡中简单而巧妙的技术

[![Here's what's going on inside your bank card. The variable capacitor is shown at top centre, and the chip is sittling in its pick-up coil on the left.](img/abf777ff607e594fd5acdeebe26ca79a.png)](https://hackaday.com/wp-content/uploads/2021/10/nfc-bank-card.jpg)

Here’s what’s going on inside your bank card. The variable capacitor is shown at top centre, and the chip is sitting in its pick-up coil on the left.

大多数标签和最便宜的阅读器模块都很少努力将它们调谐到共振，但我为这篇文章检查的一个更有趣的标签，一张被黑客空间朋友拆除的银行卡，显示了一种非常聪明的自动调谐方法。银行卡是由两层塑料层压而成的标准芯片卡，芯片触点出现在正面。在拆卸时，可以看到芯片及其触点在一小片约 10mm×10mm 的塑料上，可以从卡上取下。

这个模块可以被读卡器读取，但只有当它直接放在天线上时，而不是像在商店里那样，整个卡的任何部分都靠近读卡器。为了确保小芯片模块可以通过卡整个表面上的读卡器供电，卡的后半部分是一个印刷电路板，这是一个简单的调谐电路，带有一个大线圈和一个由一排小 PCB 板制成的巧妙的可变电容器。线圈一半绕在卡片边缘，一半绕在芯片周围，这样线圈就可以在很大的区域内接收磁场，并将产生的能量紧密耦合到芯片中。它是在制造过程中通过切割连接电容器的迹线来调谐的，据猜测这将是一个自动化的过程。测量其谐振，结果是略高于 13.56 MHz，但由于测量是在没有芯片的拆卸卡上进行的，谐振点很可能已经上移。

## 调整 NFC 阅读器以获得最大烟雾

[![A pair of cheap NFC reader modules. The one on the left has been modified to provide resonance at 13.56 MHz.](img/b63b1777aea7cc70048c4996648025a0.png)](https://hackaday.com/wp-content/uploads/2021/10/nfc-cheap-readers.jpg)

A pair of cheap NFC reader modules. The one on the left has been modified to provide resonance at 13.56 MHz.

对于读者来说，更昂贵的设备有一个内置的可变电容器，并在工厂调谐到 13.56 MHz，而便宜的模块通常有一个固定的电容器，谐振频率更高。使用这些廉价模块的经验表明，它们通常会与更简单的卡(如无处不在的 MiFare Classic)进行交互，但它们无法提供足够的能量来为更智能的卡(如 MiFare DESfire 标签)供电。将模块上的天线调整为 13.56 MHz 的谐振将效率提高到可以读取更高功率标签的程度，例如图中是由 hackerspace 朋友准备的廉价读取器模块。他使用射频拾波线圈和示波器来测量 13.56 兆赫载波的振幅，并调整调谐电路，直到振幅达到最大值。在这种情况下，他缠绕自己的线圈，并从线圈中取出导线，以找到最大值，但同样的结果也可以很容易地用 PCB 线圈和一个小微调电容器来完成。这种廉价的读卡器现在可以与以前需要昂贵得多的模块的 DESfire 卡一起工作，这使得这一过程非常值得。

因此，虽然 NFC 标签的大部分技术魔力在于其数字电子封装，但值得记住的是，让它全部工作仍然是一个牢固的模拟天线。用你的示波器和信号发生器做一点老式的射频调整工作，就能让它们的性能变得更好。