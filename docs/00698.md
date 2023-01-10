# 将 M5Stack 放在 LoRa 和物联网上

> 原文：<https://hackaday.com/2018/09/29/putting-m5stack-on-lora-and-the-things-network/>

LoRa 是低功耗、长距离通信领域的新热点。想要让数据包飞起来，[Xose]面临着一个频率问题，最终[为 M5Stack 系统开发了一个欧洲友好的 LoRa 模块](https://tinkerman.cat/m5stack-node-things-network/)。硬件旨在接入[物联网](https://www.thethingsnetwork.org/)，这是一个基于 LoRa 的网络，为物联网设备提供连接。虽然存在用于 LoRa 的现有 M5Stack 模块，但它仅支持 433 MHz。因为[Xose]在欧洲，所以需要 868 MHz 或 915 MHz 的无线电。为了解决这一问题，我们构建了一个定制板来将 HopeRF RFM69 系列模块连接到 M5Stack。

如果你以前没听说过， [M5Stack 平台](http://m5stack.com/)是一个可堆叠的开发板平台。像 Arduino 一样，您可以通过使用标准接头堆叠 PCB 来增加功能。与 Arduino 不同，M5Stack 非常适合放在箱子里，是为构建具有用户界面的设备而设计的。只需 35 美元，你就可以获得一个基于 ESP32 的系统，配有 WiFi、蓝牙、彩色液晶显示器、电池、按钮、扬声器和 IO 连接器。

硬件就位后，[Xose] 3D 打印了一个定制的盒子来容纳电路板，并将其添加到堆栈中。固件充当物联网的监视器，显示实时覆盖。最终产品看起来非常干净，保持了 M5Stack 的成品外观。

该项目的固件、电路板设计和机箱设计文件都可以在 Github 上获得[。](https://github.com/xoseperez/m5stack-rfm95)