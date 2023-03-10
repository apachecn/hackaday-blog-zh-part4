# ESP8266 为老式家庭影院增加了网络控制

> 原文：<https://hackaday.com/2020/03/06/esp8266-adds-web-control-to-old-home-theater/>

曾经有一段时间，你可以在这十年的大部分时间里拿着电视或 A/V 接收器，而不会觉得自己错过了最新最棒的功能。但是今天你很幸运，在“智能”电视被大幅改进的版本取代之前，或者成为一些奇怪问题的受害者之前，你可以使用三年，这意味着你需要买一台新的。

[![](img/1e82f41533aa9126486e664a3bcbd5b8.png)](https://hackaday.com/wp-content/uploads/2020/03/denon_detail.jpg)

A simple touch interface hosted on the ESP8266

不满足于计划淘汰的现状，[aamarioneta]最近开始着手为大约 2008 年的 Denon AVR 2308 家庭影院接收器添加少量现代便利。像任何好的 A/V 接收器一样，AVR 2308 的背板上有一系列令人眼花缭乱的端口，其中一个恰好是外部红外接收器。这被证明是 jack 在 ESP8266 中的完美位置，为这位 12 岁的接收器赢得了物联网的荣誉会员资格。

有趣的是，这种攻击实际上不涉及 IR。当然，代码可以用来驱动连接到 ESP8266 的 GPIO 引脚的 IR LED，AVR 2308 会做出响应，就好像正在使用原始遥控器一样；但是这有什么意思呢？多亏了接收器端口，他们能够将红外代码直接注入设备。这是相同的协议，只是没有光子。

在 ESP8266 上运行一个简单的网络界面，他们可以在家里的任何地方通过智能手机的浏览器控制 AVR 2308。从这里开始，只需要再多几行代码就可以将它绑定到现有的家庭自动化系统中，或者添加对 Alexa 语音控制的支持。

我们喜欢看到为旧硬件添加现代功能的[项目，因为这是一件少了一件的设备，因为它的所有者觉得它们落后于潮流。](https://hackaday.com/2020/01/27/esp32-serial-interface-modernizes-old-equipment/)[消费者变得有点不友好](https://hackaday.com/2020/02/24/ethics-whiplash-as-sonos-tries-every-possible-wrong-way-to-handle-iot-right/)，任何将权力交还给所有者的事情都是朝着正确方向迈出的一步。