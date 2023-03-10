# TAK 生态系统:军事协调走向开源

> 原文：<https://hackaday.com/2022/09/08/the-tak-ecosystem-military-coordination-goes-open-source/>

近年来，你可能已经看到了一些平板电脑和智能手机绑在士兵盔甲上的照片，尤其是美国特种部队。大多数设备上装载的主要应用程序是 ATAK 或安卓战术突击包。它允许士兵查看和共享地理空间信息，如友军和敌军位置、危险区域、伤亡情况等。作为一种处理地理空间信息的方式，其民用应用变得显而易见，如消防和执法，因此 [CivTAK/ATAK-Ci](https://www.civtak.org/) v 被创建，[于 2020 年](https://github.com/deptofdefense/AndroidTacticalAssaultKit-CIV)开源。由于 ATAK-Civ 是为那些不携带军队配发的武器的人设计的，这个首字母缩略词神奇地变成了安卓*团队意识*套件。这引起了开源社区的注意，所以今天我们将深入到成长中的 TAK 生态系统，它的怪癖和潜在的用例。

![](img/691163efe29ad019066a8813f93aa782.png)

Tracking firefighting aircraft in 3D space using ADS-B (Credit: [The TAK Syndicate](https://www.youtube.com/watch?v=v5jXQGUUeA0))

TAK 生态系统包括 Android 的 ATAK、iOS 的 iTAK、Windows 的 WinTAK，以及越来越多的服务器、插件和工具来扩展功能。TAK 的核心是目标协议，这是一种基于 XML 或 Protobuf 的消息格式，用于在客户端和服务器之间共享信息。这可能包括“目标”的位置、区域和路线信息、传感器数据、文本消息或医疗后送信息等。像 ATAK 这样的客户可以根据需要处理这些信息，还可以生成成本数据与其他客户共享。一个 TAK 客户端也可以是一个传感器节点，或者一个简单的[节点——红色流](https://www.youtube.com/watch?v=5i-y3Nc01Hs)。这意味着 TAK 可以成为监视、跟踪或控制你周围事物的强大工具。

![](img/5d2ee59e2293e5303fb02f9f2a3cedc3.png)

Standalone tools: Checking line-of-sight and camera coverage

ATAK 本身就是一个强大的制图工具。它可以在 3D 地图上显示和绘制信息，计算目标的方向，设置地理围栏，并作为团队成员之间的消息传递应用程序。除了用于户外导航，我还广泛使用了另外两个内置的地图功能。视域允许您规划无线节点位置，并检查它们的视线覆盖范围。“传感器”(摄像机)标记便于规划闭路电视装置的覆盖范围。然而，当你添加插件来扩展功能，并在网络中链接客户端来共享信息时，ATAK 开始真正闪耀。

## 建立工作关系网

要允许客户端之间联网，您需要设置一个多播网络或一个所有客户端都连接到的中央服务器。多播通信的一个流行选项是建立一个免费的零层 VPN 或任何其他 VPN。对于客户端-服务器拓扑结构，有几个开源的 TAK 服务器可以安装在 Raspberry Pi 或任何其他机器上，包括最近在 GitHub 上开源的官方 [TAK 服务器](https://github.com/TAK-Product-Center/Server)。 [FreeTakServer](https://github.com/FreeTAKTeam/FreeTakServer) 可以通过其内置的 API 和可选的 Node-RED 服务器进行扩展，并包括一个易于使用的“零接触”安装程序。Taky 是另一个轻量级的基于 Python 的服务器。所有这些服务器还包括数据包服务器，用于向客户端分发较大的信息包。

## 插件

如果你要去的地方没有互联网连接，有几个离网网络插件可用。HAMMER 充当音频调制解调器，使用廉价的宝丰收音机发送 CoTs。 [Atak-forwarder](https://github.com/paulmandal/atak-forwarder) 与基于 LoRa 的 [Meshtastic](https://hackaday.com/2020/02/26/lora-mesh-network-with-off-the-shelf-hardware/) 无线电一起工作，或者你可以使用 [APRS-TAK](https://github.com/niccellular/aprstak) 与业余无线电。

插件也可以从其他来源获取数据，比如来自 RTL-SDR 的 ADSB 数据，或者来自无人机的[视频和位置信息。许多目前可用的插件不是开源的，只有在同意美国联邦政府的条款和条件后，才能通过 TAK.gov](https://github.com/FreeTAKTeam/FreeTAKUAS)网站[获得。幸运的是，这意味着开源替代品有很大的发展空间。](http://TAK.gov)

为了进一步探索，FreeTAK 服务器背后的团队维护了一个[与 TAK 相关的工具、插件、信息源和硬件的广泛列表](https://github.com/FreeTAKTeam/openTAKpickList)。

## 入门提示

在撰写本文时，ATAK 明显比 iTAK 和 WinTAK 更成熟，所以如果你想开始探索，这是最好的选择。iTAK 实际上更容易立即开始使用，但它缺少许多功能，并且无法加载插件。

第一次在 Android 上打开 ATAK 很快就会发现，它的使用并不十分直观。我不会用一个完整的教程来烦你，但是我会分享一些我觉得有用的技巧。首先，RTFM。许多功能和工具的用法并不明显，因此附带的 PDF 手册(设置>支持> ATAK 文档)可能会派上用场。还有一个很长的设置列表可以自定义，使用设置菜单顶部栏中的搜索功能可以更容易地进行导航。

默认情况下，ATAK 没有地图，所以下载并导入[【约书亚·富勒】的 ATAK 地图包](https://github.com/joshuafuller/ATAK-Maps/releases)。这给了 ATAK 一个广泛的地图来源列表，包括谷歌地图和 OpenStreetMaps。ATAK 还可以缓存地图和影像以供离线使用。默认情况下，ATAK 仅包含低分辨率的高程数据，但是您可以从美国地质调查局网站[下载并导入](https://www.youtube.com/watch?v=1pgaGbGBZb8)更详细的高程数据。

为了与其他对 TAK 感兴趣的人联系，你也可以查看一下 [TAK 社区不和谐服务器](https://discord.gg/TVgXkcRezD)。

你在 TAK 生态系统中玩过什么吗？请在下面的评论中分享你的经验和想法。