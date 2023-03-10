# 从头开始构建一个 6.5 位数的电压表

> 原文：<https://hackaday.com/2019/11/05/building-a-6-5-digit-voltmeter-from-scratch/>

在最初致力于制造一个现代化的捷克斯洛伐克 4 位 Metra M1T242 电压表的复制品后，[Jaromir Sukuba]认为既然他在做这件事，他还不如制造一个能力稍微强一点的电压表。这导致了一个全新的 6.5 位电压表设计的设计和建造，[Jaromir]在 eev blog 上记录了这个设计。

数字板采用了 [MSP430FR5994](http://www.ti.com/product/MSP430FR5994) MCU，输入端采用了 Altera/Intel[EPM 240t 100](https://www.digikey.com/product-detail/en/intel/EPM240T100C5/544-1146-ND/703853)CPLD 加 ADC，目前该设计已经通过了一段时间的验证。当前版本在多斜率启动配置的集成 ADC 设置中使用 OPA140 运算放大器，但[Jaromir]计划在未来以更高效的拓扑结构用另一个运算放大器取代该输入板。

![https://www.eevblog.com/forum/metrology/diy-6-5-digit-voltmeter/?action=dlattach;attach=749583;image](img/74dd9e6e92449325f90a35c2fa3ccfbe.png)

验证电压表是真正的挑战，需要确定 ADC 噪声和测量的整体稳定性。在这里，验证设计的能力当然受到可用测试设备质量的限制。由于没有“完美”的水平，这意味着总会有进一步改进的空间，对于这样的 DIY 仪表来说，这既是福也是祸。

[Jaromir]已经通过 EEVBlog 页面提供了原理图和源代码(固件和 Verilog HDL ),允许任何人从他们自己的版本开始，甚至为项目做出贡献。也就是说，假设对原型系统内部的一个观察还没有让您对这样一个项目的复杂性充满敬意。

(感谢 大卫·古斯塔菲克 送来这张照片)