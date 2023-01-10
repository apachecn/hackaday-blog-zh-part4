# GCore:制造更少挫折的便携设备

> 原文：<https://hackaday.com/2022/07/09/gcore-make-portable-devices-with-less-frustration/>

[丹·胡里奥]的[g Core](https://github.com/danjulio/gCore)(T2 小工具核心的简称)旨在让基于 GUI 的便携可充电小工具更容易开发。gCore 是[Dan]自己需要一种不那么烦人的方式来开发这种硬件的结果。

[![](img/dc617d389233021eef6779c6e8979853.png)](https://hackaday.com/wp-content/uploads/2022/07/gcore_lifx_remote.png)

A touchscreen is great, but high-quality power control and charging features are what really make a portable device sing.

[Dan]发现他似乎总是在开发板中加入许多额外的电路，只是为了获得良好的电源管理和充电控制。为了解决这个问题，他为便携式设备设计了自己的通用硬件平台，于是 gCore 诞生了。

虽然彩色触摸屏是一个引人注目和有用的附加功能，但他的设计中真正的明星是电源管理和充电功能。与大多数开发硬件不同，gCore 智能地将负载功率与充电功率共享。通电和断电也全部由软件控制。

听起来很有趣？这还不是 gCore 所能提供的全部，您可以从 hackaday.io 的项目页面了解更多信息(该页面对设计决策和概念进行了更深入的讨论。)在[【丹】的网站](http://danjuliodesigns.com/projects/gcore.html)上也有一些附加的照片和细节。

[Dan]对开发硬件并不陌生。tcam-mini 热像仪是他的作品，我们毫不怀疑 gCore 的设计和特性直接来自[Dan]的实际开发需求。