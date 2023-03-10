# 你可以有两台收音机，为什么只有一台？

> 原文：<https://hackaday.com/2018/07/28/why-have-only-one-radio-when-you-can-have-two/>

Arduino 和类似平台有多种无线电屏蔽，但它们通常只支持一种协议、制造商或频段。Jan grome 在他看到的一个项目中对此感到烦恼，于是决定制造一个能够支持多种不同类型的[盾牌。因为越多越好，他还为两个不同的无线电模块留出了空间。他称由此产生的 Arduino 无线电瑞士军刀为风筝提供保护，他在 hackaday.io 页面和](https://hackaday.io/project/159940-kite-shield)[GitHub 知识库](https://github.com/jgromes/KiteShield)上分享了风筝所需的一切。

目前支持的有 ESP8266 模块，HC-05 蓝牙模块，RFM69 FSK/OOK 模块，SX127x 系列 LoRa 模块包括 SX1272，SX1276 和 SX1278，XBee 模块(S2B)，他声称更多的正在开发中。由于其中一些在非常相似的频带上工作，因此注意到它们的近距离使用是否会产生任何不利影响将是很有意义的。我们怀疑不会有，因为所涉及的协议被设计成具有弹性，但是没有什么像真实世界的例子来证明这一点。

这个项目是独一无二的，所以我们努力寻找以前类似的 Hackaday 功能。然而，我们已经看了[选择正确无线技术的概述](https://hackaday.com/2016/05/05/which-wireless-tech-is-right-for-you/)。