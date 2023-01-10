# 用于 STM32 的 Fusion:通过 WiFi 进行调试和编程的开发板

> 原文：<https://hackaday.com/2020/06/02/fusion-for-stm32-development-board-with-debugging-and-programming-via-wifi/>

MikroElektronika 显然将自己定位为 STM32 开发板世界的兰博基尼或法拉利，他们的 Fusion 开发板[的当前(第 8)版本于去年发布](https://www.mikroe.com/blog/fusion-for-stm32-v8-development-board)，不仅支持闪存，还支持通过板载 WiFi 模块调试连接的 STM32 MCU。这家塞尔维亚公司对不带 [MCU 模块](https://www.mikroe.com/blog/new-mcu-card-standard-makes-it-possible-to-use-mcus-regardless-of-their-vendor)或任何其他外设的裸板的定价似乎在 300 美元/欧元左右。额外的 MCU 板每块价格在 28-60 美元之间。

正如官方产品页面所解释的，该板与 CodeGrip 软件相结合，可以通过 USB-C(免驱动)和 WiFi 来管理该板，USB-C 还允许用户配置 WiFi 选项。外围设备板通过 5 个板载 [MikroBUS](https://en.wikipedia.org/wiki/Mikroelektronika) 扩展槽添加，既可以是现有板，也可以是定制的 MikroBUS 板。电源也是板载的，通过 USB、筒式插孔连接器或外部电池供电。

使用 WiFi 连接到主板将允许它在比办公桌更不方便的位置时易于管理和调试，这似乎是一个主要的好处。

显然，这不是一个便宜的板，每个 MCU 卡的成本大约相当于 st 的 Nucleo 或 Discovery 板的成本，因此很难证明购买它只是为了专业环境。然而，这里诱人的事情可能是如此多的设计细节是可用的，从扩展总线到 MCU 卡的引脚排列和原理图 ( [STM32F767ZG 版本](https://download.mikroe.com/examples/full-featured-boards/8th-generation/schematic/schematic-mcu-card-for-stm32.pdf))。

MCU 卡使用 [Hirose FX10A-168S-SV](https://www.hirose.com/product/p/CL0570-0244-7-00) 和 [FX10A-168P-SV(71)](https://www.hirose.com/product/p/CL0570-0044-8-71) 连接器，这些都是现成的。这使得开发兼容的 MCU 卡成为可能。一个 MCU 卡模板项目例如可以在这里找到[。](https://github.com/MisterHW/FX10AMCUCT)