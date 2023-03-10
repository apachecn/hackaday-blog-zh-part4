# 一个不寻常的智能灯泡的大脑移植

> 原文：<https://hackaday.com/2020/12/07/a-brain-transplant-for-an-uncommon-smart-bulb/>

到目前为止，这种硬件黑客已经变得足够常见，以至于不起眼，他们拿一个智能灯泡或其他电源可切换的设备，用 Tasmota 等开源软件替换其固件。但是，当发现一个新设备[有一个不受任何开源对等设备](http://www.lucadentella.it/en/2020/11/27/modificare-una-lampadina-smart-parte-1/)支持的微控制器时，该怎么办呢？如果你是(卢卡·登特拉)，你不会认输，再买一个已知处理器的，而是对它进行足够的逆向工程，给它移植一个 ESP8266 模块。

有问题的 Fcmila 品牌智能灯泡被发现具有相对未知的中国 SoC，Opulinks OPL1000。由于它甚至不能提供一个串行端口，为它编写软件是不值得的，所以他花了一段时间逆向工程它的原理图和电气协议，然后[移植到一个 Wemos D1 ESP8266 板](http://www.lucadentella.it/en/2020/11/29/modificare-una-lampadina-smart-parte-3/)。他制作了一个关于这个项目的视频，你可以在视频中间看到。

令人欣慰的是，市场上的大多数智能灯泡似乎使用更熟悉的硬件[，可以相对容易地闪烁](https://hackaday.com/2020/02/11/custom-firmware-for-cheap-smart-bulbs-is-a-cinch-to-tinker-with/)。

 [https://www.youtube.com/embed/qNNDqV81rhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qNNDqV81rhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

