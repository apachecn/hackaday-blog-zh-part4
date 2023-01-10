# MQTT 深潜

> 原文：<https://hackaday.com/2019/07/25/mqtt-deep-dive/>

如果您阅读 Hackaday，那么您很可能听说过 MQTT——消息队列遥测传输。如果你以前没有使用过 MQTT，你应该看看 Ably[Kayla Matthews]的帖子，标题是 [MQTT:一篇概念性的深度论文](https://www.ably.io/concepts/mqtt)。她确实在最后提到了他们的 MQTT 协议连接器，并对 Ably 的产品做了一些说明，但这篇文章的大部分内容都是普通的白皮书，有很多有用的信息。

当然，MQTT 之所以出名，是因为它非常小，与更重的协议相比，它的功耗最小。当您试图从一个必须在硬币电池上使用一年的设备上提供或消费数据时，MQTT 是您的朋友。

我们喜欢这份白皮书是因为它涵盖了设计系统时必须做出的架构决策。有一个标题为“什么时候可以使用 MQTT？”另一篇题为“什么时候不应该使用 MQTT？”最后，这篇文章甚至介绍了如何使用 Mosquitto、MQTT.js 和 MQTTnet。

[埃利奥特·威廉姆斯]在他的[最小 MQTT](https://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/) 系列中报道了 MQTT。我们也看到了很多像[这个门铃](https://hackaday.com/2017/03/02/wireless-doorbell-hacked-into-hands-on-mqtt-tutorial/)这样的教程项目。