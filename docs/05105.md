# 仪表板加密狗拆卸揭示硬件需要爆裂英里

> 原文：<https://hackaday.com/2019/12/16/dashboard-dongle-teardown-reveals-hardware-needed-to-bust-miles/>

汽车应用中计算机的进步和扩散几乎使遮阳树机制成为过去的遗迹。很少有人敢于面对 1999 年左右之后生产的汽车的发动机舱，更少有人敢于深入仪表板后面的空间。更令人遗憾的是，因为有人可能试图用这些邪恶的控制器局域网(CAN 总线)加密狗之一来逆转里程表。

通过[通常的销售渠道](https://www.ebay.com/sch/i.html?_from=R40&_nkw=can+filter+18+in+1&_sacat=0&LH_BIN=1&_sop=15)销售，并作为“CAN 总线过滤器”进行营销，【大克莱夫】得到了一个从 2015 款梅赛德斯 E 级轿车上拆下来的过滤器，一名机械师在那里发现它安装在组合仪表和 OEM 线束之间。当加密狗被移除时，里程表立即增加了 40，000 公里，暴露了某人的不诚实。

[大克莱夫]随后拆卸的单位表明，显着不需要欺骗一个 CAN 总线里程表。该板仅包含一个 STM32F 微控制器、一对 CAN 总线收发器芯片和一些支持电路，如稳压器。该设备连接到一个线束，该线束在拾取 CAN 总线时不受干扰地穿过仪表组的大多数线路，该设备可以欺骗仪表板显示器显示它想要的任何数字。真正有趣的是代码，对此[克莱夫]并不深究。这很遗憾，但正如他指出的，很可能是设计者在微控制器上设置了锁定位来掩盖他们的踪迹。小偷之间没有荣誉可言。

我们发现这种深入汽车世界黑暗角落的行为非常迷人，而且(大克莱夫)的修养一如既往地一流。如果你需要了解 CAN 总线的基础知识，可以看看[【Eric even chick】的汽车网络黑客系列](https://hackaday.com/2013/10/21/can-hacking-introductions/)。

 [https://www.youtube.com/embed/f4af1OBU5nQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f4af1OBU5nQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[rasz_pl]给我们发了一条这方面的提示。谢谢！