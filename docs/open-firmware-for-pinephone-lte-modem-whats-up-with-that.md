# PinePhone LTE 调制解调器的开放固件–这是怎么回事？

> 原文：<https://hackaday.com/2022/07/12/open-firmware-for-pinephone-lte-modem-whats-up-with-that/>

[在他们的月度公告中，](https://www.pine64.org/2022/06/28/june-update-who-likes-risc-v/)在所有很酷的东西 Pine64 中，他们谈到了 PinePhone 的 LTE 调制解调器的开放固件。固件没有完全开放——有几个部分保持关闭状态。Pine 强调，他们既没有预装也没有正式认可这个固件，PinePhones 将继续使用供应商提供的调制解调器固件映像。

也就是说，新的固件更有特色——它有更少的错误，更多的功能，更低的功耗，并且它的专有部分很少。我想指出的是，有了这个固件的特殊构建，PinePhone 的调制解调器可以运行 Doom——因为，嗯，当然。

有了这些，安装这个固件变得更加容易了—[现在有了`fwupd`钩子！](https://dylanvanassche.be/blog/2022/pinephone-modem-upgrade/)你可以把`fwupd`看成是固件的 Windows Update 的等价物，除了不滥用，针对 Linux。换句话说，这是保持开源设备尽可能发挥功能的完美选择。

怎么回事？如果开放固件更酷，为什么我们的手机没有开放固件选项？

# 怎么回事？

电话调制解调器相当复杂。你的手机，无论是数字平板电脑还是“智能”手机，都有一个来自联发科或高通的调制解调器芯片，该芯片内部有一个相当强大的 CPU 内核。例如，如果您使用 SIM800 调制解调器(一个仅支持 2G 的调制解调器模块)，它具有[mt 6260 芯片组、](https://hackaday.com/2015/01/01/reverse-engineering-a-superior-chinese-product/)一个 ARM7 单核 CPU 和 GSM 基带芯片。你可以把它想象成一个类固醇的 ESP8266，但是对于 GSM 来说。

在 SIM800 模块中，该 CPU 充当“接收 AT 命令并执行 GSM 操作”的中介，但它也用作 GPS 跟踪器、智能手表和其他 GSM 连接设备的万能处理器。事实上，MT6260 可以运行整个诺基亚 3310！准确的说是 2017 版。

![Render of the Quectel modem chip, top side render overlaid over the bottom side render, showing some of the pads on the bottom of the modem](img/e9266935c653227765775705b738be0e.png)

对于 PinePhone 调制解调器，情况也是如此。人们很快发现，Quectel 调制解调器在其 ARM 内核上运行一个精简版的 Android，通过调制解调器的 USB 接口提供`adb`外壳。当一些敢于冒险的黑客开始探测它并获得 shell 访问权限时，他们发现了像`ffmpeg`、`vim`、`gdb`和`sendmail`这样的编译工具——当然不是你在蜂窝调制解调器上需要的东西，但是嘿。固件映像被解包，一些代码被逆向工程，调制解调器得到了一个新编译的 Linux 心脏。

为 PinePhone 的 Quectel EC25-G LTE 调制解调器提供动力的特定芯片是高通的 MDM9207，带有单核 CPU 和 256 MB 的 RAM 和闪存—[这个 Pine64 Wiki 页面](https://wiki.pine64.org/wiki/PineModems#Quectel_EG25-G_Modem)将让您了解技术细节。如果你仔细想想，PinePhone 实际上并不是一个四核 CPU 设备——它是一个五核双 CPU 设备，并行运行两个 Linux 安装。是的，你的安卓手机也不是不可能。

# 这为什么有价值？

为什么重视蜂窝调制解调器固件的开放性呢？有人可能会说，没有它，我们也过得很好。原来，调制解调器的开放固件带来了大量的好东西！

其中最值得一提的是能够降频 PinePhone 调制解调器的 CPU 内核，将其从 400 MHz 降至 100 MHz。这使得调制解调器消耗更少的能量，并且不会使手机过热。调制解调器的配置(例如音频比特率)变得更加动态，不再需要重新启动调制解调器来更改音频参数。有各种开发人员友好的特性，如日志功能和测试设施；PinePhone 的集成也可以得到改善，即在 PinePhone 的 CPU 暂停以进一步提高电池寿命的同时，调试和改善呼叫处理。

当然，还有厄运。

 [https://www.youtube.com/embed/GvLlP6BEPPk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GvLlP6BEPPk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



也有可能解决阻碍 PinePhone 蜂窝功能的许多问题——因为它往往是蜂窝调制解调器，有大量的固件问题。其中一些问题可以通过使用不同的供应商固件映像来解决，但是在二进制映像之间寻找故障最少的映像是一项令人沮丧的工作。修补漏洞也是可能的，比如半年前 PinePhone 攻击目标为[的奇怪恶意软件](https://hackaday.com/2021/12/16/pinephone-malware-surprises-users-raises-questions/)所利用的“使调制解调器不可操作”漏洞。

![A mini-PCIe card with this Quectel modem soldered onto it](img/356919bf5e32e1d617eedcac2da6a2be.png)

You can get one of these modems standalone on a mPCIe card!

明确地说，这是大规模手机制造商已经获得的对嵌入手机的调制解调器的控制。一个开放的手机项目*必须*拥有这种控制——否则，它注定处于不利地位，纯粹是因为依赖于带有各种故障和错误功能的专有固件映像。没有固件的可修改性，开放式手机在功能对等上又多了一个障碍，我们的技术已经对开放式手机相当敌视。

在这个固件中并不是所有东西都是开放的。基带固件，也被称为 ADSP 固件的 RF 位，仍然是封闭的，还没有被任何人逆向工程-你还不能在这个调制解调器上运行 OpenBTS。

TrustZone 内核也是封闭的——我的理解是它是由高通签署的。然而，Linux 的安装是全新的，不再令人讨厌，高通的应用程序堆栈似乎已经被一个更轻量级的所取代——消除了对[封闭用户空间工具或驱动程序的任何需要，](https://xnux.eu/devices/feature/modem-pp-reveng.html)也是如此。这是一个固件，你可以在许多方面根据你的需要进行修改，[然后自己编译和刷新。](https://github.com/Biktorgj/pinephone_modem_sdk/blob/kirkstone/docs/HOWTO.md)

我一直在列举所有这些背景和好处——想想看，我还没有回答介绍问题有点不公平。为什么我们没有更早地拥有调制解调器开放固件？好吧，我们终于知道“为什么”了。

# 监管违规

PinePhone 调制解调器的开放固件在技术上更胜一筹，在代码方面，基带，也就是射频路径不会改变。那么，为什么不从工厂装运这个固件呢？为什么是“未经官方认可或推荐”的事情？答案是，如果认可或预装该固件，Pine64 可能会在某些国家失去监管批准——这就是为什么他们不这样做。

![A blue PCB with a Pi Pico and the Quectel modem on it, an IPS screen above the modem, and a few other bits&pieces like connectors](img/ff3c74f0867bf7501ccc243a0768fd70.png)

You can get one of these modems on a Pi Pico shield, even!

按照现在的情况，期望 Pine64 认可这个固件是愚蠢的。他们努力确保 PinePhone 在尽可能多的国家获得认证——如果没有预先建立的代表网络和手机制造商可以从中受益的能力，这是一项复杂的任务。如果你能够合法地运行这个固件，祝你好运——否则，所有可能的责任，不管多么不可能，都将由你承担。在 Hackaday 上，我们陶醉于作为一个私人个体去做那些你不能用出售的装备去做的事情的自由。

一个这样的领域是无线电相关固件。美国 FCC 对常规 WiFi 路由器固件[的指示导致路由器制造商试图限制你安装 OpenWRT](https://hackaday.com/2016/02/26/fcc-locks-down-router-firmware/) 。也就是说，路由器应该有可能保持定制固件友好，但我并不乐观。观察这些年的趋势，注意到固件越来越被锁定，我一直在思考一个问题。

# 难道厂家就是不费心？

了解蜂窝调制解调器制造商可以规避监管限制是很重要的。除了所有的借口和法律，还有努力的问题。带有某些限制的开源调制解调器固件并非不可能，而是制造商没有动力去费力去开放它。法律是可以变通的——我们非常清楚营销部门不缺乏法律创造力。当固件限制法获得通过时，企业的游说力量并没有显示出来，当它们面临利润损失时，这种游说力量是相当大的。为什么不在这里？

我所看到的被用作借口的是蜂窝技术的纯粹复杂性——这是有一定道理的。这些标准确实很复杂。然而，它并不需要涉水通过蜂窝协议的细微差别来降低调制解调器的 CPU 频率，或修复接口错误。它的某些部分可能是开放的，或者至少是开源的，然而他们不是。

![A TP-Link router with its cover taken off, jumper wires going from its PCB to a breadboard, that a logic level shifter PCB is plugged in. Other set of wires from the shifter then seems to go into a USB-UART adapter.](img/610685abfbd60421dd94fb68b736f4e9.png)

We’re moving away from OpenWRT-flashed routers capable of years-long uptime

另一个借口是法规遵从性，这也站得住脚-但是，我们从来没有开始讨论，也没有承认我们的需求，以及可以和应该讨论的需求。一些调制解调器有一个 SDK，集成商可以使用，一些调制解调器将为您提供某种代码解释器，甚至——通常情况下，访问这些文档需要建立业务关系，然后，监管问题似乎不是一个很大的障碍。

许多以法规遵从性为借口的问题碰巧让制造商在财务上受益——无论是通过因计划淘汰而出售的新硬件，还是没有花在技术上他们没有被迫投入的努力上的资金。固件定制停留在 NDA 和业务关系之后，而不是至少部分开放和有竞争力。这非常适合垄断玩家。

固件开放是一个致力于它并克服障碍的问题——如果制造商不愿意付出努力，至少我们黑客可以在这里或那里进行补偿。现在，如果我们想要开放手机的功能对等，我们将不得不使用逆向工程工具——在某些方面深入专有固件。

# 为什么不

你可能想知道——为什么是现在，为什么是 Pine64？之前也有过开源基带项目，但能走到这一步的不多。嗯，有几个因素对他们有利，我想谈谈主要的一个。

![Screenshot of the PinePhone product listing from the Pine64 store, showing that it currently sells for $150](img/1feff7de2968942add1726566cea66d7.png)

It’s hard not to appreciate a $150 open smartphone

将硬件交到黑客手中是实现这些突破的关键——这正是 Pine64 成功做到的。PinePhones 已经推出两年多了，基本上每个想要的人都可以得到一部，导致相当多的黑客拥有一部内置 Quectel 调制解调器的开放式设备。

从那以后，黑客开始戳调制解调器只是时间问题！低廉的价格也有所帮助——尽管与旗舰手机相比，PinePhone 没什么好惊讶的，但它的价格也只是旗舰手机的一小部分，而且在它上面安装 Linux 有助于在性能方面发挥更大作用，消除了如果它运行 Android 会更显著的缺点。

我还想补充一点，以如此低的价格拥有一部黑客朋友手机，意味着你可以让特定类型的黑客使用它，这些黑客已经习惯于从他们拥有的设备中榨取越来越多的东西——出于经济原因等。有时，我们的技能会因需要而变得更强，这也是 Pine64 所做的工作更有价值的原因之一——帮助新一代黑客访问他们以前在经济上无法进入的工具和游戏场所。

# 新机遇

很有可能你的一部私人手机也能以同样的方式被黑客破解——去掉运行你手机调制解调器的劣质 Linux 版本，换上你更能控制的 Linux 版本。PinePhone 的可用性帮助我们克服了这个障碍，现在未来的项目将从中受益。事实上，您可以将这些 Quectel 调制解调器中的一个作为 mPCIe 卡，并轻松地将开放固件调制解调器构建到您自己的设备中！

这个固件并不是完全开放的，但它的很大一部分是开放的——这恰好是对改进 PinePhone 的蜂窝功能最有用的部分。有了这样的可修改性，我们下一步要实现什么呢？有了这些能力，我们将来会面临什么样的挑战？我们还不知道会发生什么，但这项工作对我们来说是个好消息。