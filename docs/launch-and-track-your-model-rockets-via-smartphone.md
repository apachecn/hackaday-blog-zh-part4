# 通过智能手机发射和跟踪你的模型火箭

> 原文：<https://hackaday.com/2022/07/27/launch-and-track-your-model-rockets-via-smartphone/>

制作和飞行模型火箭非常有趣。然而，最终，火和烟的刺激消退了，你想知道更多关于它在空中做什么。出于对知识的渴望，[archy587]开始建立一个项目来监控飞行中的火箭的重要数据。

该项目在火箭中安装了一个 M0 羽毛微控制器板，以及一个 900 MHz LoRa 发射器和一个 GPS 模块。这使得火箭的行程可以被测量和记录，并且在降落伞回收过程中当飞行器漂离靶场时特别有用。船上还有一个继电器模块，它从一个专用的独立电池向火箭发动机点火器提供能量。这使得火箭可以无线发射。

在地面上，该装置使用一个装有另一个 LoRa 模块的 ESP32 来接收来自火箭的信号。它旨在通过 USB-C 端口连接到 Android 智能手机。这使得从火箭接收的数据可以显示在 Android 应用程序中，包括覆盖在谷歌地图上的火箭 GPS 位置。

能够远程点燃你的火箭并跟踪它们的进展给发射台带来了一些高科技的酷。你将很快用[微型飞行控制器和矢量推力升级你的火箭](https://hackaday.com/2021/09/05/three-stage-thrust-vectoring-rocket/)。只要确保你使用的任何技术都符合你所在地区的模型火箭规则。

 [https://www.youtube.com/embed/Z9_dJVolPos?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Z9_dJVolPos?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

