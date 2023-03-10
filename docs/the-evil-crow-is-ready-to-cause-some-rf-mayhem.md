# 邪恶的乌鸦准备好引起一些射频伤害

> 原文：<https://hackaday.com/2021/04/27/the-evil-crow-is-ready-to-cause-some-rf-mayhem/>

毫无疑问，RTL-SDR 项目使无线电黑客比以往任何时候都更容易获得，但你只能用一个重新设计的电视调谐器。显然，最大的缺点是你只能听信号，而不能传输信号。如果你准备伸出手去接触某人，但不一定想把钱花在 HackRF 这样的东西上，[邪恶的乌鸦 RF 可能是你理想的下一步](https://github.com/joelsernamoreno/EvilCrow-RF)。

这种知识共享许可板将两个 CC1101 无线电收发器和一个 ESP32 结合在一个方便的包中。无线电让你可以使用 300 到 928 MHz 之间的频率(有一些间隙)，事实上有两个频率意味着你可以在一个频率上收听，而在另一个频率上传输；为传递信号开辟了有趣的可能性。使用标准固件，您可以连接到运行在 ESP32 上的 web 界面，以配置基本的接收和传输选项，但还有一个更高级的 RFQuack 固件，允许您通过运行在主机上的 Python 来控制硬件。

[![](img/567b843da4f2fc2ebf8bd81efd6945ec.png)](https://hackaday.com/wp-content/uploads/2021/04/evilcrowrf_detail.jpg)

Using the Evil Crow RF without a computer.

一个特别好的功能是位于 Evil Crow RF 侧面的一系列按钮。由于该设备与 Arduino IDE 兼容，您可以轻松地修改固件来为按钮分配各种功能或操作。

[在首席开发人员【Joel Serna】](https://twitter.com/JoelSernaMoreno/status/1343573202967126022)的演示中，当设备插入标准 USB 电源组时，物理按钮被用来触发重放攻击。秘密行动有很大的潜力，这是有道理的，因为该设备是在考虑 pentesters 的情况下设计的。

作为一个开源项目，你可以自由构建自己的 Evil Crow RF，但那些寻求更全面体验的人可以从全球速卖通订购组装板，价格为 27 美元。这种硬件制造方法似乎在开源人群中越来越受欢迎，[开放智能手表提供了类似的选择](https://hackaday.com/2021/04/08/an-open-source-smart-watch-youd-actually-wear/)。

【感谢 DJ Biohazard 的提示。]