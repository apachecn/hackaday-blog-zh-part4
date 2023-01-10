# 从 NFC 数据记录器下载，无需应用程序

> 原文：<https://hackaday.com/2021/09/23/download-from-nfc-datalogger-no-app-required/>

过多的无线技术使互联网连接设备成为标准，但如果你不需要实时更新，这并不总是必要的。无论是因为电池寿命，还是位置和范围的限制，只要有可能，直接从设备上下载数据可能是一个可行的解决方案。[Malcolm Mackay]展示了一个关于开源 [cuplTag](https://www.crowdsupply.com/cupl/cupltag) 温度/湿度记录器的优雅解决方案，使用任何支持 NFC 的智能手机，无需定制应用程序。

cuplTag 利用支持 NFC 的智能手机上的功能自动打开 cuplTag 提供的 URL。它将来自传感器单元的传感器数据编码为一个大约 1 kB 的 URL 中的循环缓冲区，该缓冲区自动上传到绘制数据的 web 前端。(你可以用他们的服务器，也可以自己运行。)

这意味着任何人都可以通过合适的手机收集数据，无需任何设置。数据显示在 web 应用程序上，并可以以 CSV 格式下载。为了防止欺骗，每个标签都带有一个密钥，用于在每次循环缓冲区改变时生成一个唯一的 HMAC。

电池寿命是 cuplTag 的一个优先事项，理论上，使用电流啜饮的德州仪器 MSP430 微控制器，它能够在单个 CR1220 硬币电池上运行七年。硬件[，固件](https://github.com/cuplsensor/cupltag)，服务器端[前端](https://github.com/cuplsensor/cuplfrontend)和[后端](https://github.com/cuplsensor/cuplbackend)代码都是开源的，可以在 GitHub 上获得。

今年早些时候，我们举办了一场数据记录比赛，展示了从你花园的湿度到你的咖啡因摄入量的各种监测。