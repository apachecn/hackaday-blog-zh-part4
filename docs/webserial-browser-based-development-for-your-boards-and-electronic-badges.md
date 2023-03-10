# WebSerial:基于浏览器的电路板和电子徽章开发

> 原文：<https://hackaday.com/2021/03/21/webserial-browser-based-development-for-your-boards-and-electronic-badges/>

多年来，与开发板对话的最容易实现的方法之一是给它一个串行端口。几乎所有的东西都有某种形式的序列，所以所需要的就是启动一个终端。但是即使如此简单，最终用户仍然会发现终端界面有些令人生畏。例如，考虑一个针对孩子的展板，或者一个必须让尽可能多的人能够接触到的活动徽章。

我们已经看到了 WebUSB 形式的解决这个问题的非常方便的解决方案，但对于没有适当 USB 硬件的设备，有 WebSerial，这是一种浏览器内 API，用于与串行端口(包括 USB 转串行芯片)进行通信。[【Tom Clement】认为这可以作为活动徽章的发展方向](https://pixel.curious.supplies/blog/webserial/)。最重要的是，它可以进行改造，以便为带有串行端口的旧徽章或开发板进行浏览器内开发。

他演示该技术的电路板是运行 badge.team 固件平台的一系列活动徽章，包括他自己的来自 CampZone 2019 的 [i-Pane](https://hackaday.com/2019/07/25/campzone-2019-badge-is-begging-to-become-a-huge-billboard/) ，以及直接追溯到[的 SHA 2017 徽章](https://hackaday.com/2017/05/08/the-sha2017-badge-revealed/)，但没有理由为什么相同的技术不能扩展到其他电路板。

然而，这一切都有一个障碍，可悲的是，在撰写本文时，只有 Chrome 家族的浏览器支持它，Mozilla 和苹果没有计划，微软也保持沉默。因此，情况看起来可能会保持不变。然而，不可避免的是，随着时间的推移，将会有商业产品通过使用廉价的 USB 串行芯片来利用它，所以也许合并它的情况将会出现。

表头:莫比乌斯，[公有领域](https://commons.wikimedia.org/wiki/File:Serial_cable_(blue).jpg)。