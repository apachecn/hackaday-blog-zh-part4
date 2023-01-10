# 用谷歌助手控制非谷歌设备

> 原文：<https://hackaday.com/2019/01/07/controlling-non-googley-devices-with-google-assistant/>

在不久的将来，智能家居将可以用你的声音控制任何东西。假设一切都支持你选择的智能家居标准，也就是。如果你有一个支持其他标准的设备，你最终会对它大喊大叫。除非你用 [gBridge](https://about.gbridge.io/) 。顾名思义，gBridge 是谷歌助理设备和智能家居世界其余部分之间的桥梁。这是一个[开源项目](https://github.com/kservices/gBridge)，可以作为 Docker 镜像在家中的低功耗设备或托管服务上运行。

从根本上说，gBridge 是 MQTT 翻译器的谷歌助手。消息队列遥测传输(MQTT)是许多智能家居设备使用的消息协议，因为它运行在 TCP 上，并且实现起来不需要太多的能量。我们已经介绍了如何在 MQTT 中尝试并自己完成大部分工作[这里](https://hackaday.com/2018/08/24/how-to-mash-up-ble-nodejs-and-mqtt-to-get-internet-of-things/)，但是 gBridge 看起来更容易使用。它刚刚从 beta 测试中出来，看起来它可能是进入智能家居黑客的一个好方法。

当然，还有很多其他方式可以做到这一点，例如[IFFT](https://hackaday.com/tag/ifttt/)，但 gBridge 背后的大脑【Peter Kappelt】声称，它更灵活，因为它提供了对整个谷歌助手词汇的支持，所以你可以用非谷歌设备做一些事情，比如将设备分组，或者进行更多条件控制(例如如果走廊的光线水平超过一定程度，就开始用相机记录)。[Peter]还希望将 gBridge 作为一项托管服务来运营，在那里他负责更新服务器等幕后工作，收取少量费用。

 [https://www.youtube.com/embed/OPh4I9JpEoc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OPh4I9JpEoc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

