# EMF 营地的 GSM 电话网络基于 Raspberry Pi 和 LimeSDR 构建

> 原文：<https://hackaday.com/2018/08/30/gsm-phone-network-at-emf-camp-built-on-raspberry-pi-and-limesdr/>

英国的电磁场 2018 黑客营将拥有自己的 GSM 电话网络，正如我们已经报道的[，它的徽章将是一部全功能的 GSM 电话](https://hackaday.com/2018/08/26/2018-electromagnetic-field-badge-its-an-entire-phone/)。据我们所知，这是世界上第一个徽章，虽然它可能不是黑客阵营连接的第一个，但在基站方面仍然是一个不小的成就。为了找到更多的信息，我们采访了网络背后的两个人，一个是无线电方面的[Lime Microsystems](https://limemicro.com/)’【安德鲁·贝克】，另一个是网络方面的 [Nexmo](https://www.nexmo.com/) 的开发者倡导者【萨姆·麦金】。

有 16 个基站分布在站点周围，其中每一个都是带有 LimeSDR Mini 的 Raspberry Pi 3 B+该系统的开发是在 Raspberry Pi Foundation 的 PoE 板发布之前进行的，因此他们采用独立的 24V 电源，通过直流-DC 转换器为 Pi 供电。如果需要任何长电缆，这种布置允许显著的电压降。

在软件方面，所有基站都运行 [Osmocom](https://osmocom.org/) (开源移动通信)蜂窝基站基础设施包。这是一体化 [Osmocom NITB](https://osmocom.org/projects/osmonitb/wiki/OsmoNITB) 封装和完全模块化 Osmocom 之间的一个很好的决定，因为前者的可靠性而选择前者。有人评论说，在未来的活动中不一定是这种情况，但在目前是有意义的。它在网络上显示为 SIP 电话系统，这意味着它可以很容易地与现有的 DECT 网络集成。让我们从用户端来看看网络是如何运作的，以及让一切成为可能的许可漏洞。

## 电话号码和虚名号码

作为用户，你会发现一张 SIM 卡和你的徽章，来自物联网连接提供商[全息图](https://hologram.io/)。这是一个用于公共网络的全功能 SIM 卡，但它仅用于访问活动网络，现场不需要全息注册。我们被告知，网络不实现商业网络的基于 SIM 的加密，因此理论上任何 SIM 都可以在网络级别上工作，但是提供的一批全息 SIM 在大小上是可管理的，它们在网络上是单独授权的。

![](img/860d66f08e7e7c9baa83a21c088eebf7.png)

Everyone at Electromagnetic Field 2018 gets one of these GSM phone badges. Read [Hackaday’s first look at the hardware](https://hackaday.com/2018/08/26/2018-electromagnetic-field-badge-its-an-entire-phone/).

用户将收到一个 5 位数的号码，但是你可以在“电磁场 2018 电话簿”(称为 [Eventphone](https://guru3.eventphone.de/) )中注册你选择的 4 位数号码，并将其与你的 GSM 号码绑定。对于黑客日，我们已经注册了 4096 个。我们被告知，将有一个向外连接，提供免费电话到英国，美国和欧洲，并将有通过网关号码接入。还将有一系列特殊号码用于音频馈送和其他现场设施，他们希望让 [Jasmin 短信到 HTTP 网关](http://www.jasminsms.com/)运行，为使用徽章的应用程序提供可黑客攻击的接口。没有 GSM 数据连接，因为任何数据都可以通过现场无线网络更有效地传输。每个基站只能同时处理 7 个呼叫，由于 GSM 数据流占用呼叫信道，如果启用数据，很快就没有可用的语音带宽。看看有没有人在夏令营期间黑进他们自己的手机数据系统，这将会很有趣！

## 许可频谱

也许围绕网络的最有趣的背景故事来自它被许可的方式。任何有能力建立 Osmocom 的人都可以创建自己的 GSM 网络，但对于电磁场这样的事件，它必须是官方批准的事情，以避免所有相关人员陷入法律困境。

在手机行业的几次合并之后，英国有四家主要的网络提供商，获得网络许可证可能是一件极其昂贵的事情，价格标签高达数十亿英镑。多年来，由于不同的政治体制管理着这个体系，这个体系中出现了一些意想不到的怪癖。最有用的怪癖之一是所谓的[并发网络接入](https://www.ofcom.org.uk/manage-your-licence/radiocommunication-licences/mobile-wireless-broadband/concurrent-spectrum-access)许可。这些是在 1800 MHz 范围内的一种特殊类型的低功率许可，在 GSM 和 DECT 分配之间的一个最初留作保护频带的分配中是空的。其他蜂窝许可频率范围由持有这些频率范围的运营商独占，而这一频率范围则由同时使用它的多个被许可方共享。有许多许可证持有者，包括一些意想不到的小玩家以及大玩家，它是这些公司中的一家，它已将其许可证出租给该活动。

## 复杂网络惊人的简单

这个网络给我们留下了深刻的印象，它的硬件实现相对简单，它将提供有用的功能，以及他们获得许可证的方式。我们知道，像黑客营的所有系统一样，许多工作已经投入其中，我们谨代表所有与会者感谢所有相关人员让它发生。我们期待着看到你们会用它做什么。