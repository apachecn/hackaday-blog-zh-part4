# 使用 Pwnton Pack 追踪 WiFi 中的幽灵

> 原文：<https://hackaday.com/2022/05/28/track-down-ghosts-in-your-wifi-with-the-pwnton-pack/>

如果你的网络邻居有什么奇怪的事情，你会打电话给谁？如果你想时尚地诊断你的 WiFi 问题，试着打电话给[特拉维斯·考恩]——他可能会穿着令人惊叹的 Pwnton 包出现。它由一个类似于 1984 年经典*捉鬼敢死队*中使用的复制质子包构建而成，它是一个便携式无线安全诊断工具，应该能够找出无线网络中的任何弱点。

在内部，它有一个 Mark VII WiFi 菠萝，这是一个为安全测试目的而设计的便携式设备，还有一个运行 [Pwnagotchi](https://hackaday.com/2020/09/30/automated-tools-for-wifi-cracking/) 的 Raspberry Pi:一个基于深度学习的 WiFi 嗅探器，旨在捕捉那些有助于最大限度地增加暴力破解 WPA 密钥的机会的网络数据包。这两个设备连接到一个天线阵列，包括一个很酷的旋转 5 GHz 面板天线，以扫描周围地区。

当然，Pwnton Pack 还包括一个 Neutrona Wand，在这种情况下，它包含一个 2.4 GHz 的八木天线，连接到一个 ESP32，编程为执行身份验证攻击。一个 Arduino Nano 驱动一个 LED 矩阵，显示滚动的 *Pac-Man* 幽灵，而一个专用的声卡提供电影音效。整个系统由三个 LiPo 电池组供电，如果需要，甚至可以远程操作。

可悲的是，它没有附带那些鬼陷阱来吸收任性的 WiFi 网络，但可用的工具范围应该有助于捕捉任何类型的怪异幽灵隐藏在您的系统中。在之前，我们已经发现了几个[质子包，但从来没有一个具有如此先进的功能。毕竟，安全测试系统倾向于](https://hackaday.com/2016/06/27/ghostbuster-proton-pack-made-from-everything/)[少*一点*显眼](https://hackaday.com/2021/05/06/putting-an-ultra-tiny-linux-board-in-a-phone-charger-eventually/)。

 [https://www.youtube.com/embed/_6QAVOaUOnM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_6QAVOaUOnM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

