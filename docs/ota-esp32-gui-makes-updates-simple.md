# OTA ESP32 GUI 使更新变得简单

> 原文：<https://hackaday.com/2020/06/23/ota-esp32-gui-makes-updates-simple/>

拥有像基于 ESP32 的廉价 WiFi 功能板的一个缺点是，你必须更新它们。如果你家里每个房间都有几个，把它们拔出来并连接到电缆上进行编程可能会很痛苦。空中编程是一个很好的答案，[Kevin]展示了如何通过一个简单的 GUI 来控制更新。你可以在下面看到它是如何工作的视频演示。

[Kevin]使用现成的 OTA 库来完成这项工作，但是创建了一个 GUI 配置和下载器工具。有一个手动步骤可以强制电路板进入 OTA 模式，这可能有点不方便，但它提高了安全性，因为您需要实际接触器件才能进行更新。

GUI 使用 Processing 的 Python 模式，并为 Windows、Linux 或 Mac 生成。当然，您可以使用命令行界面来完成同样的工作，这对于人工操作人员来说可能更令人畏惧，但与自动化系统集成起来会容易得多。例如，您可能希望将更新作为 Makefile 的一部分。

你确实需要在工作站上安装 Java 来让一切正常工作。我们以前见过 [ESP32 OTA](https://hackaday.com/2019/03/21/library-makes-esp-over-the-air-updates-easy/) 做过。你甚至可以用 Arduino 来玩[一样的特技。](https://hackaday.com/2018/01/18/over-the-air-updates-for-your-arduino/)

 [https://www.youtube.com/embed/iMPBpUdL-rk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iMPBpUdL-rk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

