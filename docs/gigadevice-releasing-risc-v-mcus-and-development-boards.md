# GigaDevice 发布 RISC-V MCU 和开发板

> 原文：<https://hackaday.com/2019/08/27/gigadevice-releasing-risc-v-mcus-and-development-boards/>

可能没有太多人听说过中国制造商 GigaDevice，到目前为止，它主要是一家 NOR 闪存制造商。然而，他们的 GD32 系列 MCU 兼容 STM32，这使他们成为直接从 ST 采购的有趣(更便宜)的替代方案。现在，GigaDevice 在一次演示中宣布，他们将发布一系列基于 RISC-V 的 MCU:GD32V 系列。

由于 [GigaDevice](https://en.wikipedia.org/wiki/GigaDevice) 还没有更新他们的[英文网站](https://www.gigadevice.com/)，我们所拥有的信息是基于 *CNX 软件*从中文的翻译[。他们列出了 GD32VF103 系列 MCU 的规格如下:](http://gd32mcu.21ic.com/news/detail/new_id/161)

*   内核–GD 32 VF 103 RISC-V“大黄蜂内核”@ 108 MHz
*   内存–8KB 至 32KB SRAM
*   存储–16KB 至 128KB 闪存
*   外设–USB OTG 和 CAN 2.0B
*   I/O–3.3V，5V 容差
*   电源电压–2.6 至 3.6V
*   封装—qfn 36、LQFP48、LQFP64、LQFP100 封装

它们是否与 GD32 MCUs 引脚兼容仍有待确认。如果事实证明是这样，那么对于某些产品来说，这可能是一个有趣的嵌入式解决方案。从规格来看，他们似乎很清楚他们的目标是低端的基于 ARM 的 MCU，如 ST 的基于 Cortex-M3 的 [STM32F103](https://www.st.com/en/microcontrollers-microprocessors/stm32f103.html) ，这在许多嵌入式系统中非常常见。

看到这两种类型的 MCU 之间的性能比较将是有趣的，因为与 ARM 内核相比，其功耗更低，效率更高。MCU 和开发板都已经在天猫有售，基本的 [GD32VF103C-START 板](https://detail.tmall.com/item.htm?spm=a1z10.4-b-s.w5003-21978304610.1.48fa306cBtYGKJ&id=601020356481)售价约为 11 美元，GD32VF103TBU6 MCU (QFN36，64 kB 闪存)售价约为 1.27 美元。

在这一点上，英文文档和 SDK 似乎有点缺乏，但希望不久我们也能使用这些 MCU，而不必上中文课。

感谢[Flaviu]的提示！