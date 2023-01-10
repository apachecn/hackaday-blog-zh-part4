# 你被邀请去控制很多圣诞树

> 原文：<https://hackaday.com/2018/12/24/an-iot-christmas-tree-youre-invited-to-control/>

我们喜欢物联网设备，但偶尔也会担心它们可能会让不良黑客有机可乘。在这种情况下，[Kevin]创建了[一个物联网树，允许任何人控制灯光模式](http://kevincuzner.com/iotree/)，他邀请您这样做！

我们玩了一下树，网页界面相当强大。对于每个 LED，您可以选择随机颜色或关键帧定义的图案。对于关键帧 led，您可以创建多个“关键帧”，每个关键帧都由一种颜色和过渡来定义，可以是线性、四分之一正弦波或瞬时(“墙”)。可以为每个 LED 添加额外的关键帧，如果不为所有 LED 指定模式，系统会重复您已定义的关键帧来填充整个字符串。如果您喜欢，也可以选择一些预设模式。如果你也想玩这棵树，不要拖延:它只在 2019 年的第一周可用！

在幕后，一个老化的 Raspberry Pi 提供了驱动 LED 控制器和视频流的本地大脑，而运行 [Redis](https://github.com/antirez/redis) 实例的云服务器允许与网络通信。WS2811 LEDs 灯串的接口使用【凯文】的 [Kinetis LK26 分线板](https://github.com/kcuzner/kl2-dev)，尽管 Kinetis ARM 系列的工具和文档状态不佳，他还是设法让它工作。你可以在[的博客](http://kevincuzner.com/2018/12/21/the-iotree-an-internet-connected-tree/)上读到关于这个系统的很好的讨论；需要协同工作的部分多得惊人。像往常一样，他在 GitHub 上提供了这个项目的所有[源代码。](https://github.com/kcuzner/iotree)

我们以前看过[凯文]的作品，包括他的[73 LED 手表](https://hackaday.com/2018/07/05/leds-make-an-analog-wristwatch/)，以及在 STM32 上从头开始开发的[冒险](https://hackaday.com/2016/06/05/learning-arm-without-dev-board/)。

但是，如果是很多圣诞树引起了你的思考，你可以看看去年的这棵圣诞树。