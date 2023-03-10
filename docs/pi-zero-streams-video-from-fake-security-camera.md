# Pi Zero 从“假”安全摄像头中获取视频流

> 原文：<https://hackaday.com/2019/06/20/pi-zero-streams-video-from-fake-security-camera/>

假的安全摄像头被宣传为一种廉价的方式来阻止任何可能不怀好意的人。这不是一个罪与罚的博客，所以我们真的不能说这种说法实际上有多准确，但我们看到足够多的这些东西出售，一定有人相信它们值得拥有。不过，如果是我们，我们会从[丹尼尔·安德拉德]那里得到这个建议，用树莓 Pi 和 WebRTC 把我们的“假”相机转换成真相机。

[![](img/3f55fd94cd1f760a10e65a9958ab79c2.png)](https://hackaday.com/wp-content/uploads/2019/06/picam_detail.jpg) 这些假相机的品牌和型号数不胜数，但似乎它们中的许多都有一个相当共同的设计，那就是它们使用的外壳实际上对放置你自己的硬件非常有用。它们是中空的，相对来说受到良好的保护，因为大多数都使用闪烁的 LED 或其他功能来使它们看起来更真实，它们已经有一个功能电池盒。

事实证明，[丹尼尔]花 9 美元买的这个非常适合 Raspberry Pi Zero 和它的相机模块。他甚至将闪烁的 LED 连接到 Pi 的 GPIO 引脚，这样它看起来仍然像一个部件，尽管用 RGB LED 和适当的脚本来驱动它将是一种很好的方式，可以获得一些关于系统正在做什么的视觉反馈。

软件方面的工作由 Balena 完成，Balena 是一套用于设置和管理 Linux 物联网设备的工具。它们提供了一切，从运行在 Pi 上的 SD 卡映像到将所有数据整合在一起的云基础设施。当去年[他创造了他的比特币交通灯](https://hackaday.com/2018/11/22/this-bitcoin-price-tracking-traffic-light-isnt-just-a-red-led/)的时候【丹尼尔】稍微深入了一点软件栈。

对于任何可能对这个项目有似曾相识感的读者来说，你并没有发疯。我们最近看到了一个类似的项目，[使用了一个 ESP8266 和一个 PIR 传感器来为其中一个假相机添加运动感应功能](https://hackaday.com/2019/05/22/dummy-security-camera-is-smarter-than-it-looks/)。现在我们只需要有人把一个 Arduino 放在其中一个里面，我们就有了神圣的三位一体。