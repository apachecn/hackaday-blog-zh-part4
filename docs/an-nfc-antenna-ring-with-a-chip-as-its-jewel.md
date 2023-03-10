# 以芯片为宝石的 NFC 天线环

> 原文：<https://hackaday.com/2021/12/10/an-nfc-antenna-ring-with-a-chip-as-its-jewel/>

在过去十年中，通过支持 NFC 的银行卡进行非接触式支付使我们的日常交易变得更加方便，但仍然存在找到卡并在读卡器上挥舞的繁琐任务。也许嵌入式芯片对我们许多人来说太远了，但在可穿戴设备(如戒指)中使用银行卡怎么样？[Jonathan Limén]向我们展示了如何从银行卡中取出 NFC 芯片模块，并将其安装在一个嵌有线圈天线的戒指上。

银行卡中的芯片安装在一个小而薄的 PCB 上，一侧有触点，另一侧有一个线圈作为天线。它不够敏感，无法与大多数读卡器一起可靠地工作，因此该卡包含一个单独的印刷电路层，形成一个大型调谐电路，耦合到芯片天线。在用丙酮将芯片从卡上移除后，他继续通过在环上缠绕线圈来制造卡天线的替代品。这变成了一个试错的过程，但最终，结果是一个工作的 NFC 支付环。

我们很喜欢这个想法，但我们会尝试用矢量网络分析仪消除一些试错，并运行几圈导线作为芯片的更紧密耦合线圈。这是我们之前在 Hackaday 上讨论过的一个主题，我们不介意再来一次。