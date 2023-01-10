# Arduino MKR 让 Nespresso 监控变得简单

> 原文：<https://hackaday.com/2021/04/25/arduino-mkr-makes-nespresso-monitoring-easy/>

用微控制器监控电器通常遵循一条老路:潜入电器内部，在电路中找到可以通过某种接口连接到微控制器的地方。对于他的 Nespresso pod 咖啡机，【Steadman】避免撕扯设备，而是选择监测它发出的声音。一个商品声音阈值传感器板连接到一个 Arduino MKR 零，这个设置记录咖啡消费。值得注意的是，这一代 Arduino 不再是老式的简单电路板，而是在其 SAMD21 Cortex-M0+处理器旁边配备了 RTC 和 SD 卡，因此非常适合这样的数据记录项目。咖啡数据可以保存到 CSV 文件中，可通过电子表格查看，并提供了代码。

我们喜欢这个项目，因为它的非侵入性简单，我们可以看到，可能有许多其他类似的机器可以受益于非侵入性监测的模拟技术。虽然 Hackaday 的页面上充满了咖啡机项目，但我们看到的豆荚咖啡机却少得惊人，这可能是因为我们的读者是一群精明的人，他们不愿为自己的咖啡因支付额外费用。如果你碰巧有一台 Nespresso 咖啡机，[也许你需要一些帮助来识别胶囊](https://hackaday.com/2017/02/19/nespresso-capsule-detector/)。