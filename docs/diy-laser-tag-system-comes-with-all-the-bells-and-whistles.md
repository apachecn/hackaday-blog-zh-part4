# DIY 激光标签系统配备了所有的铃铛和哨子

> 原文：<https://hackaday.com/2021/01/07/diy-laser-tag-system-comes-with-all-the-bells-and-whistles/>

虽然虚拟现实变得越来越身临其境，但它仍然无法与一款老式的激光游戏相媲美，无法让你热血沸腾，也无法与朋友共度美好时光。[Xasin]已经致力于 DIY 激光标签系统有一段时间了，它已经发展到包括一系列令人印象深刻的功能和可定制性。

该项目名为 LZRTag，始于 2018 年，在试验板上使用简单的基于 ATmega328 的原型。它已经发展成为一个功能齐全的系统，3D 打印手枪中的 ESP32s 通过 MQTT 与 Raspberry Pi/Linux 游戏服务器进行通信。每支手枪还配有一个加速度计，I2S 音频放大器和扬声器用于游戏声音，以及 ws 2812 RGP led 用于灯光效果。红外激光器被用作发射器来瞄准可佩戴的红外接收器，更多的 RGB LEDs 被连接到手枪上。

Linux 机器上的 Ruby 服务器负责所有的通信、游戏管理、镜头验证和评分。它可以容纳多达 255 名玩家，并且在游戏模式、武器种类或者你想要的任何其他特性方面都是非常可定制的。[Xasin]还创造了红外信标来增加更多的可能性，例如捕捉旗帜、安全区域和复活区域。

我们真的很喜欢这个系统的灵活性，它会成为黑客空间的一个很棒的团队项目。你也可以增加一个[电击模块](https://hackaday.com/2017/07/04/a-shocking-wizard-duel/)来激励玩家避免被击中。如果你想要更多的枪，看看今年早些时候我们在展示的[带头盔显示器的激光标签步枪](https://hackaday.com/2020/02/06/custom-laser-tag-rifle-packs-a-sonic-punch/#comments)

 [https://www.youtube.com/embed/uVn6aU2ZVG8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uVn6aU2ZVG8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

