# 被水獭咬过的纳米机器人

> 原文：<https://hackaday.com/2020/02/01/a-nano-with-an-otters-bite/>

当涉及到他们项目的微型开发板时，未来的微控制器实验者现在面临着一系列令人困惑的选择。从最初的 Arduino 的后代和克隆到诸如 Raspberry Pi Zero 和类似的主板的全脂肪 Linux powerhouses 都可以拥有，而且通常价格合理。

现在有一个新成员加入了竞争，[otter pill 是一个基于 STM32F072 的板，具有类似 Arduino-Nano 的引脚排列](https://github.com/Jana-Marie/OtterPill)，它来自[Jana Marie]的工作台。面对如此多的竞争对手，你可能会问自己它能提供什么，这将是一个有效的观点，因为纳米克隆可以以相对低廉的价格获得。除了 ARM Cortex M0 的 Nano shield 兼容性和额外的功能之外，它还是一款开源开发板，USB-PD 包含在其 USB-C 插槽中，通过一些精英 BoM 魔法，她成功地将其组件的成本降低到了 3 美元以下。[USB-PD 示例固件已经发布](https://github.com/Jana-Marie/USB-PD-Firmware)，空白固件也即将发布。目前，这款主板还只是原型，但是如果你也想要的话，她正在组织生产。我们在秋天的 eth0 看到了它的早期发展[，考虑到自那以后的进展，我们确信我们不用等太久。](https://hackaday.com/2019/11/03/eth0-autumn-2019-tiny-camp-creative-badge/)

普通读者会认出[Jana Marie]的作品，因为水獭主题的版块以前也出现过。我们最近的产品是[将 USB-PD 带到 TS-100 烙铁的 USB-C 替代板](https://hackaday.com/2019/12/26/adding-usb-c-to-the-ts100-but-not-how-you-think/)，以及[一个漂亮的可寻址 led 小 USB 板](https://hackaday.com/2019/12/24/addressable-led-strings-in-your-usb/)。