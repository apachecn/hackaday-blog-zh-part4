# BeOS:另一个宇宙的麦克·OS X

> 原文：<https://hackaday.com/2020/01/09/beos-the-alternate-universes-mac-os-x/>

你可能对史蒂夫·乔布斯如何被苹果公司驱逐并创办自己的公司 NeXT 的老故事很熟悉。苹果随后收购了 NeXT 和他们的技术，并让乔布斯再次担任首席执行官。然而，乔布斯的道路并不是独一无二的，从那以后，计算机的历史可能会完全不同。

1990 年，在苹果公司接替乔布斯担任麦金塔开发主管的让-路易·加西(Jean-Louis Gassée)也被公司解雇。随后，在另一名前苹果员工史蒂夫·萨科曼的帮助下，他成立了自己的电脑公司。他们称之为 Be Inc，他们的目标是基于 C++的面向对象设计，使用专有硬件，从零开始创建一个更现代的操作系统，该系统可以提供当时个人计算机所没有的更强大的媒体功能。

## 认识 BeOS

[![](img/70917bfb6e19caf7440939ff8cab613b.png)](https://hackaday.com/wp-content/uploads/2019/09/beos-videomail.gif)

Could you imagine emailing someone a video file in 1995? Be Inc. did.

当时，BeOS 是对家庭计算新方式的一次尝试。它引入的功能在当时是全新的，现在已经无处不在——比如抢占式多任务处理、日志文件系统和整洁的桌面设计。在某种程度上，它足够超前，如果你今天看到它的截图，你会发誓它只是任何其他现代 Linux 环境，90 年代的图形美学除外。其开发者推动的主要优势是该平台提供的多媒体支持:不仅操作系统的设计方式使得视听格式易于使用，而且硬件本身也构建有各种 I/O 端口来适应这种工作。

在双核计算机还是一个遥远的梦想的时候，第一个 BeBox 原型已经在& T 霍比特人系统作为双处理器开发出来了。霍比特人是专为 C 语言设计的短命 RISC 处理器。然而，由于 AT & T 停止了芯片的生产，Be Inc .很快将其开发转向基于 PowerPC 的系统，这就是我们今天所知道的 BeBox。

[![](img/448ac4b49023e7a5a5569823bb94d08d.png)](https://hackaday.com/wp-content/uploads/2019/12/beos-blinkenlights.jpg)

A PowerPC BeBox, including the Blinkenlights at the lower left and right of the case.

BeBox 最终于 1995 年 10 月首次亮相，采用双 PowerPC 架构，每台主频为 66 MHz，一年后推出 133 MHz 型号。为了强调拥有两个不同处理器内核的创新，其创造性形状的外壳前面有两堆称为“Blinkenlights”的 led，每个 led 都显示每个 CPU 的当前负载。最重要的是，它提供了当时其他家用电脑没有的标准接口:两个 MIDI I/O 端口，多个线路级音频通道和一个被称为“Geekport”的连接器。这个连接器是一个面向实验性电子开发的端口，具有电源引脚、两个双向 8 位通道以及 D/A 和 A/D 转换器，名副其实。

## 可能是一个竞争者

1994 年，苹果的 System 7 正在显示它的年龄。该公司投入精力开发代号为 Copland 的继任者，将作为系统 8 发布。到 1996 年，在错过最后期限和管理不善之后，该项目被认为不可行并被取消。现在，苹果正在为他们的下一个操作系统寻找外部资源，它表现出了收购 Be Inc .的兴趣，Be Inc .作为一家开创新的桌面计算模式的公司，迅速获得了恶名。面向对象的 BeOS 做了苹果希望新 Mac OS 做的一切，甚至更多。

对 Be Inc .的员工来说，不幸的是，苹果公司对这笔交易并不感冒。该公司赌上一项新技术，压低报价，只出价 1 . 25 亿美元，但被高管拒绝。当年晚些时候，苹果宣布他们将以两倍于此的价格(4.25 亿美元)收购 NeXT。当然，那笔交易包括了史蒂夫·乔布斯，这是 Be Inc .无法提供的，剩下的就是历史了。

[![](img/97615bb80d238b7b1321c851053816a8.png)](https://hackaday.com/wp-content/uploads/2019/12/beos-evilla.jpg)

The Sony eVilla, one of the appliances designed to run BeIA software.

由于缺乏收购，Be 的硬件处于商业上不可行的状态；仅售出约 1800 台后，该公司被迫将重点从硬件转向软件。BeOS 随后被移植到更常见的 x86 架构上，以应对这一变化，但销量继续下滑。

该公司最终采取了免费赠送 BeOS 并专注于 BeIA 的做法，BeIA 是 BeOS 的一个版本，旨在用于互联网设备上——但即使是这一点也不足以拯救该项目或公司。Be Inc .在 2001 年解雇了大部分员工，并将公司资产出售给 Palm，Inc .，Palm 决定不再继续该项目。除了次要版本更新 r 5.1“Dano”的泄露之外，BeOS 上的官方生产被永久关闭。

## 俳句继续前进

BeOS 的商业消亡并没有终结 Be Inc .员工的核心愿景。从那时起，一个名为 [Haiku](https://www.haiku-os.org/) 的新开源项目从零开始，从 BeOS 停止的地方开始。这个新操作系统的第一个测试版于 2018 年 9 月发布，每夜发布继续更新。新特性包括一个完整的包管理器，比如在 Linux 发行版中常见的那些，以及对更现代的媒体格式的支持。

二十年前 BeOS 的原始体验仍然可以通过模拟器重现。由于这种方法使用了后来的 BeOS x86 端口，所以您并不完全了解定制 BeBox 硬件可以为您提供的全部功能，但它仍然是对昨天的未来世界的部分一瞥。Adafruit 已经写了[一个使用 VirtualBox](https://learn.adafruit.com/build-a-bebox-with-beos-and-virtualbox?view=all) 引导你设置 BeOS R5 的指南，然而，由于我无论如何都无法让它正常工作，所以我最后用 PCem 代替写了[我自己的指南，以防那个也不适合你。](https://hackaday.io/page/6640-getting-beos-50-professional-to-work-on-pcem)

现在留给我们的是想知道，如果那么多年前，早在 1997 年，苹果决定收购 Be Inc .而不是 NeXT，今天的台式电脑生态系统会有什么不同？蒂姆·伯纳斯·李会使用 BeBox 来运行世界上第一台网络服务器吗？今天的 Mac OS X 会是什么样子，它还会有它标志性的(双关语)码头吗？或者也许技术有一个汇聚点的趋势意味着不管怎样，最终一切都会以同样的方式发展。没有办法知道，但沿着记忆之路旅行总是很有趣。