# 自制墙阻止 Roomba 和其他真空把戏

> 原文：<https://hackaday.com/2019/09/20/homemade-wall-stops-roomba-and-other-vacuum-tricks/>

如果你有一个 Roomba，你知道他们很方便。然而，他们确实有进入你希望他们避开的地方的习惯。你可以得到虚拟的墙壁，它们只是小小的红外信标，但是你也可以自己滚动。这就是[MKme]所做的，而且出乎意料的简单，尽管它可能是通向更复杂的东西的跳板。你可以在下面看到一个视频。

对于 Arduino 项目来说，这再简单不过了。一个红外发光二极管，一个电阻和一大把调用红外遥控库的代码。如果这就是你想要的，Arduino 就有点大材小用了，尽管它确实足够简单和便宜。

我们知道这并不多，但我们对与未来方向项目相关的一些其他信息印象深刻。例如，有一个项目使用手柄下的串行端口为 Roomba 添加了一个[超声波传感器。那个端口的接口和协议甚至很好地](https://create.arduino.cc/projecthub/ssbaker/making-roomba-smarter-800-series-40c5e2?ref=platform&ref_id=424_recent___&offset=11)[记录了](https://cdn-shop.adafruit.com/datasheets/create_2_Open_Interface_Spec.pdf)。

这让我们开始思考。你或许可以使用一些超声波传感器进行双向通信，来定制墙壁。例如，您可以使用一个设备每秒发送一定数量的脉冲，并让 Roomba 上的另一个设备接收这些脉冲并进行计数。例如，你可以编写规则，比如某堵墙实际上只在早上 8 点到下午 5 点之间。

我们已经看到一些人使用 Roomba 作为通用机器人平台。我们仍然希望能够在 DigiKey 目录中找到一个传感器，以帮助避免[这个常见问题](https://hackaday.com/2016/08/24/roomba-vs-poop-teaching-robots-to-detect-pet-mess/)。

 [https://www.youtube.com/embed/aEn5C83Qoro?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aEn5C83Qoro?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

