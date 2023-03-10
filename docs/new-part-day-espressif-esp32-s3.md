# 新零件日:Espressif ESP32-S3

> 原文：<https://hackaday.com/2021/01/09/new-part-day-espressif-esp32-s3/>

自从 Espressif 系统进入我们的集体意识以来，它们已经将其范围从 ESP8266 扩展到 ESP32，并超越了最初的 WROOM 和 WROVER 模块，扩展到一系列进一步的 ESP32 产品。有一种单核变体和一种包装 RISC-V 内核来代替 Tensilica 内核，现在他们已经展示了他们的最新产品。ESP32-S3 将 ESP 提升到了一个新的水平，打包了更多的 I/O，板载 USB，以及两个 Tensilica 内核的更新版本和蓝牙版本 5。它仍然是一个 ESP32，但更有用，值得仔细研究，因为我们希望它在相当多的项目中出现。

[![Espressif's block diagram for the chip.](img/ee9ab4480485a9f5adbfa3ecf3e48e8a.png)](https://hackaday.com/wp-content/uploads/2021/01/ESP32-S3_0.png)

Espressif’s block diagram for the chip.

遗憾的是，数据手册似乎还没有发布，但我们确实有一些小细节需要考虑。Espressif 急于告诉我们它的“AIOT”功能，这要归功于上一代 LX6 中没有的 [EXTensa LX7 内核](https://ip.cadence.com/uploads/1099/TIP_PB_Xtensa_lx7_FINAL-pdf) (PDF)中的矢量指令。他们声称这将加速软件神经网络；这确实有点市场营销的味道，但在看到它投入使用之前，我们不会做出判断。新的核心肯定会提供全面的性能改进，这应该是所有 ESP32 开发人员感兴趣的。与此同时，现有 ESP32 开发人员熟悉的超低功耗内核仍然存在。

然后是 USB 支持，它出现在功能框图中，但在其他地方几乎没有信息。它被列为 USB OTG，这增加了 ESP32 成为主机的可能性，但它也应该带来的是模拟其他 USB 设备的能力。我们已经看到[徽章作为 WebUSB 设备安装，使用 STM32 克隆作为 ESP32 的外设](https://hackaday.com/2020/07/31/campzone-2020-badge-literally-speaks-to-us/)，但未来这些技巧应该可以在 Espressif 芯片本身上实现。

新设备规格中最令人期待的可能是增加了 10 条新的 I/O 线。这在历史上一直是 ESP 系列的弱点，它很容易耗尽可用的引脚。这些额外的线路将使其与具有更大封装选项的 STM32 系列微控制器相比更具竞争力，也意味着设计可以在不使用端口扩展器的情况下拥有更多外设。

总之，ESP32 系列的最新成员提供了一个重要而有用的更新，并将单核版本中首次出现的一些功能带到了更强大的芯片系列中。遗憾的是，它没有所希望的片上 RAM 提升，但它带来了足够多的新功能，令人感兴趣。目前，看起来 ESP32-S3 还没有订单，但我们希望尽快获得工程样品，并在适当的时候给您带来实际操作报告。