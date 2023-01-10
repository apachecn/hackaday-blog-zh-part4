# 通过 VGA 连接器进行时间同步

> 原文：<https://hackaday.com/2019/11/10/time-sync-through-your-vga-connector/>

虽然它可能处于暮年，但古老的 VGA 视频连接器隐藏了一个多功能的接口，仍然可以为实验者提供各种黑客攻击的机会。我们还没有看到类似[flok]的东西，他使用 VGA 接口[插入定时信息，NTPd 实例从该信息中获取其引用](https://vanheusden.com/misc/blog/2019-11-07.php)。

如果因为 VGA 接口是模拟输出而不是数字输入，这似乎有悖常理，那么你闻到老鼠的味道是正确的。他在第一句话中澄清，因为他没有使用 VGA 线本身，而是使用 I ² C 接口，这是除了最基本的 VGA 卡之外的所有 VGA 卡的功能。这是即插即用操作系统识别显示器功能的方法，但很难阻止它被用于其他目的。在这种情况下，Arduino 由温度补偿晶体振荡器提供每秒 1 个脉冲的定时信号，提供由 NTPd 轮询的 I ² C 外设。

这个项目应该会引起任何修补者的兴趣，因为它提供了关于识别和使用 VGA 插座上的 I ² C 接口的宝贵信息。所以[如果你把 VGA 卡用作 SDR](https://hackaday.com/2018/04/23/spoofing-cell-networks-with-a-usb-to-vga-adapter/) ，你可能会觉得很有趣，但是[快点，否则你可能会完全错过机会](https://hackaday.com/2016/01/29/vga-in-memoriam/)。

VGA 插头图像:Swift。汞[[CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:Male_VGA_connector.jpg)