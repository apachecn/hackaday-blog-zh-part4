# 用激光束击败密码处理器

> 原文：<https://hackaday.com/2022/11/26/defeating-a-cryptoprocessor-with-laser-beams/>

在大多数情况下，密码协处理器是很好的。这些是通过 I2C 或单线连接的小芯片，实现了一整套加密功能。它们可以散列数据，安全地存储加密密钥并使用它进行内部加密/解密，签署数据或验证签名，并生成适当的随机数——所有这些都是您可能不希望在 MCU 的固件中完成的，因为您必须防范一系列攻击。从理论上讲，这很好，但这将攻击转移到了加密协处理器。

在这个 BlackHat 演示文稿 ( [幻灯片](//i.blackhat.com/USA21/Wednesday-Handouts/us-21-Defeating-A-Secure-Element-With-Multiple-Laser-Fault-Injections.pdf))中，【奥利维耶·赫里沃】讲述了他的团队是如何负责调查 Coldcard 加密货币钱包的安全性的。这款钱包将你的私人密钥存储在一个 [ATECC608A 芯片](https://hackaday.com/tag/atecc608a/)中，在一个安全的区域，只有当你输入你的 PIN 码时才会解锁。该团队已经在不同的场景中遇到了 ATECC608A 的前身 ATECC508A，最终它放弃了自己的秘密。这一次，他们能撬开金库，带着满满一袋比特币离开吗？

由于缺少一个可以钻孔的保险库门，他们使用了一个强大的激光器，去除了集成电路，并用光束脉冲照射它的不同区域。你怎么知道什么时候脉搏跳动？为此，他们对芯片的功耗进行了跟踪，经过足够的尝试和一些信号平均，让他们对芯片的固件如何通过解锁命令处理阶段做出有根据的猜测。我们不会破坏你的视频，但如果你对功率分析和激光故障感兴趣，这是非常值得你花 30 分钟的时间。

你可能会认为我们有这些芯片是件好事——然而，它们对爱好者来说并不友好，因为出于安全的原因，适当的文档很少。另一个缺点是，不可避免地，我们会遇到它们被用来阻碍修复和逆向工程。然而，如果你想探索密码协处理器带给你什么，你可以[获得一个内置 ATECC608A 的 ESP32 模块](https://github.com/espressif/esp-idf/tree/master/examples/peripherals/secure_element/atecc608_ecdsa)，我们已经看到该芯片被用于[一个支持物联网的可穿戴 ECG 项目、](https://hackaday.com/2018/10/27/new-avr-iot-board-connects-to-google/)甚至[一部诺基亚外壳的 LoRa mesh 手机！](https://hackaday.com/2021/06/26/lora-messenger-in-nokias-shell/)

我们感谢[芯片]与我们分享这一点！

 [https://www.youtube.com/embed/Kj1nVJypXPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Kj1nVJypXPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

