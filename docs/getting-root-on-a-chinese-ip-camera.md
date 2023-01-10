# 扎根于中国的 IP 摄像机

> 原文：<https://hackaday.com/2022/12/12/getting-root-on-a-chinese-ip-camera/>

有这么多廉价的联网设备都是 Linux 驱动的，通常通过一个串行接口尝试侵入它们是很有诱惑力的。这就是[Andrzej Szombierski]的目标，他购买了一台廉价的中国 IP 摄像机，使用 XM 530 ARM SoC[来探索](http://kuku.eu.org/?projects/xm530/part1)并最终[获得 root 访问](http://kuku.eu.org/?projects/xm530/part2)权限。这款相机的固件在其网络侧提供了常见的网络接口，但它的 PCB 上也有一个 UART，这要归功于未填充的四引脚接头。

当然，仅仅启动一个串行终端应用程序并连接到这个 UART 是不够的。[Andrzej]遇到的第一个障碍是 U-Boot 被配置为不输出 Linux 内核引导消息。在通过一些创造性的黑客手段解决了这个问题之后，下一个挑战是使用固件映像的转储来找出 root 密码，这导致了对用于 root 密码的固件和编码的更多探索。

即使这些挑战中的某些部分可能是偶然的，而不是制造商故意造成的，但它表明这些基于 SoC 的 Linux 设备可以进行相当激烈的斗争。这就留下了下一个问题，在您获得 root 访问权限后，如何处理这样的 IP 摄像机？