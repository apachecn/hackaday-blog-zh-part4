# 用中断支持的位碰撞动画神秘协议

> 原文：<https://hackaday.com/2022/06/19/animate-arcane-protocols-with-interrupt-backed-bitbanging/>

我们经常认为我们的“软件串行”库是理所当然的，并且不去调查在幕后发生了什么——至少直到他们让我们失望。您想了解如何利用中断驱动的位碰撞功能吗？[Jim Mack] [教导我们如何使用 LTC 协议作为跳板，让我们的协议实现飞起来](https://escmdxi.wordpress.com/2022/06/02/longitudinal-bit-banging/)。

LTC (线性/[纵向]时间码)是一种广泛使用且制作精美的协议，它往往在我们的雷达下飞行，黑客可以从中学习很多东西。它用于在媒体制作和回放期间同步音频/视频设备。LTC 的信号几乎是数字的，但不完全是数字的:它不需要时钟，也没有极性。此外，它很好地模拟了音频信号，可以以任何回放速度解码，以及[Jim]概述的许多其他优点和怪癖。不过，你确实需要保持时间，而[Jim]的文章向我们展示了如何在不影响你的主要任务的同时保持时间。

使用中断意味着您的主循环可以做其他事情，有效地让您在后台运行不同类型的任务。[Jim]使用以定义的频率触发的中断实现 LTC 协议发送器，在主循环中进行 LTC 数据处理，时间关键的 GPIO 在中断处理程序代码中摆动。他解释了代码结构和其中的细微差别，最后，他甚至为我们提供了一个高性能、可配置的 LTC 发射器项目的源代码，供我们研究和重用。无论是 RF 发射器位碰撞、IR 远程信号接收、UART 仿真，还是您的 MCU 缺少外设支持的任何其他协议，您都可以在这里学习如何让它工作。

在[Jim]的上一篇文章中，他花了很大的篇幅解释精确度和准确度的基本原理，然后使用 ATMega 将这些理论再次付诸实践。在本系列的下一篇文章中，他想创建一个 LTC 解码器，向我们传授更多关于如何正确使用中断来完成对时间敏感的任务。我们等不及了！