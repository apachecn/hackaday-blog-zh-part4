# IRC Over LoRa，当事情真的变糟时

> 原文：<https://hackaday.com/2020/12/12/irc-over-lora-for-when-things-really-go-south/>

作为一个社会，我们已经习惯了永远在线的高速数据连接，无论我们是在家里使用计算机还是在外面使用移动设备。但是，如果自然灾害摧毁了当地的基础设施，会发生什么呢？当然，如果有些人需要接触某人，他们可以打开收音机，但即使在黑客中，火腿也是少数。我们真正需要的是一个备用互联网。

CellSol 项目背后的团队希望证明[建立一个志愿者运营的分布式通信网络](http://f3.to/cellsol/)不仅在黑客社区的能力范围内，而且可能比你想象的更容易、更便宜。网络中的每个节点，在 CellSol 的说法中被称为 Pylon，可以在 LoRa 主干网和 WiFi 设备(如智能手机和电脑)之间传输数据。一旦网络建立并运行，用户不需要任何特殊的硬件或软件来使用它。

[![](img/b50ee7863f522dceaf533ef768bba3ef.png)](https://hackaday.com/wp-content/uploads/2020/12/cellsol_detail.png) 现在要澄清的是，这里没人在谈论网上冲浪。当用户连接到其中一个 ESP32 塔时，他们将能够通过浏览器访问一个简单的聊天系统。如果挂架有一个活跃的互联网连接，聊天可以被桥接到一个 IRC 频道。在没有互联网连接的情况下，这种支架只是给 CellSol 网络上的用户提供了一种相互交流的方式。为了保持简单，没有用户名，私人信息，或加密。这是最基本的、世界末日式的交流。

想加入溶胶革命吗？你真正需要的是一个 ESP32，一个 LoRa 无线电，和开源固件。如果你得到像 Heltec LoRa 32 开发板这样的东西，你甚至不需要把任何东西焊接在一起。亮出黑板就走。一旦你有了几个塔，你也可以用装备了 LoRa 的 Arduino 组装一个便宜的中继器节点。这两种设备都很小，而且足够节能，可以很容易地用电池或太阳能供电。正如你在休息后的视频中所看到的，该团队甚至设想了一个未来，他们可以通过无人机在公共场所下车。

这不是我们第一次[看到 ESP32 被用来建立离网 LoRa 通信网络](https://hackaday.com/2020/02/26/lora-mesh-network-with-off-the-shelf-hardware/)，就像以前的那些尝试一样，它的有效性将在很大程度上取决于你能说服多少人建立自己的节点和中继器。但是如果你有一些思想开放的朋友住在附近，这可能是一个很好的聊天方式。

 [https://www.youtube.com/embed/0XiAXQbfULk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0XiAXQbfULk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

