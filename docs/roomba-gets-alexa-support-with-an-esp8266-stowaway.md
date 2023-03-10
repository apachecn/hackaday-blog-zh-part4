# Roomba 通过 ESP8266 Stowaway 获得 Alexa 支持

> 原文：<https://hackaday.com/2021/03/09/roomba-gets-alexa-support-with-an-esp8266-stowaway/>

现代家庭充满了大量的“智能”设备，但不幸的是，它们并不总是说同一种语言。咖啡机和电视可能都能够通过各自的应用程序与你的手机通话，但这并不一定意味着这两种设备可以一起工作，以更好地协调你的早晨生活。这是一个遗憾，因为如果更多的这些设备可以相互通信，我们将更接近我们承诺的生活。

幸运的是，作为硬件黑客，我们可以帮助我们的设备更好地相互了解。[my home things 最近的一篇文章展示了 ESP8266 如何弥合 Roomba 和亚马逊的 Alexa 助手之间的差距](https://myhomethings.eu/en/roomba-voice-control-alexa-and-belkin-wemo-emulator/)。这不仅可以让你便宜、方便地给机器人吸尘器添加语音控制，还可以让它与亚马逊流行的家庭自动化框架兼容。这使得将设备链接在一起成为复杂的条件例程成为可能，例如在每晚的某个时间关灯并启动真空吸尘器。

黑客依赖于所谓的 Roomba 开放接口，这是一种七针迷你 DIN 连接器，可以通过部分拆卸机器人来访问。该连接器从 Roomba 的板载电池以及双向串行通信总线向控制器供电。

通过将 MP1584EN DC-DC 转换器和 ESP8266 连接到该连接器，可以直接向硬件发送命令。添加一点胶水代码，将这种能力与模拟 Belkin Wemo 设备的库结合起来，现在 Alexa 能够随意停止和启动机器人。

在之前，我们已经[见过几次这种技巧被用来为各种小工具](https://hackaday.com/2018/01/27/alexa-controls-this-projector-thanks-to-esp8266/)添加[后门 Alexa 支持，看看什么样的不寻常的硬件人们正在](https://hackaday.com/2015/07/16/how-to-make-amazon-echo-control-fake-wemo-devices/)[寻求成为他们智能家居](https://hackaday.com/2019/02/04/esp8266-and-alexa-team-up-to-tend-bar/)不可或缺的一部分总是很有趣。