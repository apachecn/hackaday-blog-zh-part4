# 苹果 AirTag 泄露秘密

> 原文：<https://hackaday.com/2021/05/10/apple-airtag-spills-its-secrets/>

苹果 AirTag 是一个 29 美元的蓝牙信标，可以粘在你的东西上，在你丢失的时候帮你定位。虽然它不仅仅是一个寻呼机，但它的想法是它可以被任何设备无声地发现——几乎就像一个众包网状网络——并且它的主人会提醒他们在世界上任何地方的位置。

尽管苹果公司一再保证，但仍有许多关于其隐私影响的问题，因此自然对研究此类事情的人有很大的兴趣。[在那些对其进行工作以获得对其 nRF52832 微控制器的控制的人中，第一个是【Stacksmashing】](https://twitter.com/ghidraninja/status/1391148503196438529)，他使用了[一种故障技术，通过精确的定时](https://limitedresults.com/2020/06/nrf52-debug-resurrection-approtect-bypass/)中断芯片的内部电源，以绕过其调试端口的内部启用保护。固件已经被丢弃，当然还有一个标签被重新用于更有价值的应用——瑞克罗林蓝牙监听器。

每个设备都有一个全球网络来帮助失主找回丢失的物品，这个想法从表面上看非常有趣，苹果公司在 AirTag 产品页面上煞费苦心地向客户保证系统的安全性。一方面，这项工作使 AirTag 成为一种为其他应用获取 nRF 微控制器的稍微昂贵的方式，但真正的价值将在分析固件以了解标签本身如何工作时体现出来。

【Stacksmashing】之前在这些页面上出现过很多次，经常是在任天堂硬件的背景下。只有一项工作是[打开任天堂游戏并观看](https://hackaday.com/2020/12/02/a-straightforward-guide-to-unlocking-the-nintendo-game-and-watch/)的指南。