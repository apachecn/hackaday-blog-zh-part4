# 廉价健身追踪器的定制固件

> 原文：<https://hackaday.com/2019/02/20/custom-firmware-for-cheap-fitness-trackers/>

可穿戴硬件的概念很有吸引力，但对于第一次制作的人来说可能很难处理。虽然我们中的许多人在设计 PCB 和焊接神秘设备方面经验丰富，但与柔软多肉的人体进行交互可能会出现无法预见的困难。当然，有一种方法可以解决这个问题——利用别人已经完成工作的现有平台。这正是[Aaron Christophel]所做的，通过逆向工程和开发廉价健身追踪器的定制固件。

[Aaron]工作的第一部分包括研究和拆卸。在网上购买了各种各样的健身追踪器后，他最终发现了他最喜欢的设备，IWOWNFIT 的追踪器 I6HRC。它具有一个 NRF52832 微控制器，以及一个 IPS 显示器，一些闪存和一个振动电机。连接是通过蓝牙低能耗处理的。[Aaron]特别称赞它的制作精良的外壳，可以拆卸而不会损坏，以及板上的备用 USB 2.0 焊盘，可用于通过 SWD 接口对设备进行编程。

[Aaron]开发了一个兼容 Arduino 的固件[,将在论坛帖子中进一步讨论。](https://translate.google.com/translate?hl=en&sl=auto&tl=en&u=https%3A%2F%2Fwww.mikrocontroller.net%2Ftopic%2F467136)已经开发了大部分板上外设，降低功耗是当前积极开发的领域。

固件破解总是很有趣—[你考虑过给你的电视定制一个开机屏幕吗？](https://hackaday.com/2018/12/07/hacking-your-way-to-a-custom-tv-boot-screen/)有 FitBit 原版而不是克隆？这也有一个[黑客](https://hackaday.com/2017/12/29/34c3-fitbit-sniffing-and-firmware-hacking/)。

感谢吉姆的提示！]