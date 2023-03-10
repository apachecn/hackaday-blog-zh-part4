# 暴露在外的 ESP32

> 原文：<https://hackaday.com/2019/11/17/the-esp32-laid-bare/>

大多数读者都熟悉 ESP32，Espressif 的双核处理器，集成了 WiFi 和蓝牙。但是很少有人会探究它的所有特性，包括它内置的加密设施和安全引导能力。有了这些，开发人员可以保护他们的代码，确保他们的设备安全。

然而，这种安全感现在可能是虚幻的，这要归功于[有限的结果],他开发了一系列对芯片的攻击，这些攻击损害了芯片的[加密核心](https://limitedresults.com/2019/08/pwn-the-esp32-crypto-core/)、[安全引导](https://limitedresults.com/2019/09/pwn-the-esp32-secure-boot/)和[闪存加密](https://limitedresults.com/2019/11/pwn-the-esp32-forever-flash-encryption-and-sec-boot-keys-extraction/)。这使得在锁定的 ESP32 设备上执行任意代码和提取固件成为可能。

为了实现这一切，他在设备的电源上使用了一种毛刺技术，在轨道上插入一个精心定时的毛刺，以符合正在执行的特定指令。对于我们这些不是这种技术专家的人来说，他提供了一个基本的入门，描述了他用 CMOS 开关芯片自制的 glitcher。

除了新的芯片，似乎没有解决这种攻击的办法，但是，应该记住的是，这是一种依赖于拥有装备良好的工作台的专业黑客的事情，因此可能只会成为制造商的一个重大难题。但它破坏了一个主要系列微控制器的关键特性，因此它仍然是一项重要的工作。