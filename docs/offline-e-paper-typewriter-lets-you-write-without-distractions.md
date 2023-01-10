# 离线电子纸打字机让你写作没有分心

> 原文：<https://hackaday.com/2019/02/18/offline-e-paper-typewriter-lets-you-write-without-distractions/>

在网上生活和工作并不总是容易的，尤其是在保持专注的时候。只需要一瞬间的软弱，点击了不该点击的东西，掉进了一个浪费时间、扼杀创造力的兔子洞。想象一下，如果不是因为下一个浏览器标签带来的吸引人的麻烦，创造性的汁液会如何沸腾。

扼杀创造力的网上诱惑对一些人来说太难以抗拒了，这就是为什么我们发现[这种自制电子打字机](https://blog.adafruit.com/2019/02/14/the-spudwrite-single-purpose-user-device-for-creating-writing-made-with-e-paper-mbed-and-stm32f401-cortex-m4/)如此吸引人。它的创造者[卢西恩]称它为“SPUDwrite”，或“单用途用户设备”，它是一个完全不连接的书写终端。在其核心，SPUDwrite 只是一个键盘，连接到 STM32F401 Cortex-M4 微控制器，运行 MBED 并驱动电子纸显示器。不幸的是，显示器的刷新率太低，看不清你在键入什么，所以[Lucian]包括了一个小的 LCD 显示器，显示当前文本和你在文件中的位置。还有一台热敏收据打印机，您只需将硬拷贝拿在手里。[卢西恩]在 Adafruit 展示和讲述会议上介绍了 SPUDwrite，在休息时间下面有一个片段。

SPUDwrite 并不完美，但[卢西恩]对第二版有计划，包括提高刷新率-[[本·克拉斯诺]可能会在这方面有一些建议](https://hackaday.com/2017/10/31/ben-krasnow-hacks-e-paper-for-fastest-refresh-rate/)。但即便如此，我们还是喜欢这种不受干扰的创造力，同时还能拥有你作品的电子副本。只要我们能避开智能手机，我们的书可能最终会因为其中一个而成为现实。

 [https://www.youtube.com/embed/5FzrRdWKHko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1028&wmode=transparent](https://www.youtube.com/embed/5FzrRdWKHko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1028&wmode=transparent)



感谢[PT]的提示。