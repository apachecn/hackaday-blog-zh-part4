# 构建串行总线以保存旧硬盘

> 原文：<https://hackaday.com/2022/06/28/building-a-serial-bus-to-save-an-old-hard-drive/>

近二十年来，通用串行总线一直是计算机外设之间发送信息的事实上的标准，尽管名称中有“通用”一词，但情况并非总是如此。在计算机世界占据主导地位之前的几十年里，包括 USB 在内的大量竞争标准已经存在，如果你试图从没有 USB 的计算机中恢复数据[，你可能必须在如何做到这一点上发挥创造性](https://www.fysnet.net/blog/2018/08/index.html#20aug2018)。

[Ben]最近遇到一个 80486，遇到了这个问题，所以他必须发挥创造力来恢复驱动器中的内容。由于它的外形，他称它为“午餐盒”电脑，虽然它没有 USB，但它有一个可靠的串行端口来与其他电脑通信。[Ben]为接收计算机和发送计算机编写了一个软件，以便通过串行链路将驱动器扇区一个接一个地复制到运行 Windows XP 的独立计算机上，并且能够通过这种方式恢复驱动器的内容。

[Ben]写的所有代码都可以在他的 GitHub 页面上找到，任何人都可以重新启动一台 30 年前的电脑。虽然这听起来不寻常，但这种老式的计算机仍然在运行像[数控机床](https://hackaday.com/2018/12/04/replace-legacy-cnc-pcs-with-a-gerbil/)或[旧主机](https://hackaday.com/2022/06/19/your-own-ibm-mainframe-or-vax-or-cray-the-easy-way/)这样的东西。