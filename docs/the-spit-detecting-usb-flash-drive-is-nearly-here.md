# 检测唾液的 u 盘快到了

> 原文：<https://hackaday.com/2022/12/25/the-spit-detecting-usb-flash-drive-is-nearly-here/>

普通读者可能记得，安全研究人员和一般开源硬件狂热者[Walker]已经计划了一段时间的一个相当不寻常的闪存驱动器——只有当用户确保在插入之前舔手指，它才会显示其内容。我们很高兴地报告，理论最近已经让位给了真正的硬件，而 [Ovrdrive“自毁”闪存驱动器现在离现实更近了一步](https://interruptlabs.ca/2022/07/29/I-m-Building-a-Self-Destructing-USB-Drive/)。

[上次我们与[Walker]](https://hackaday.com/2022/09/26/so-how-do-you-make-a-self-destructing-flash-drive/) 联系时，他还没有组装任何硬件，尽管他相当确定他需要哪些组件，以及这些组件将如何组合在一起。这在一定程度上得益于这样一个事实，即 USB 闪存驱动器是一种无处不在的技术，使它们的主要部分丰富且有相当好的记录。正如下面的视频中所解释的，你真正需要旋转自己的闪存驱动器的是 USB 连接器，控制器芯片，和一个很好的闪存板供它访问。当然，你得靠自己来检测唾液。

[![](img/c0d400426cc05ea15a08aa612267db86.png)](https://hackaday.com/wp-content/uploads/2022/12/spitdrive_detail.jpg)

The build video has some gorgeous camera work.

我们特别喜欢这个项目的是[Walker]将整个项目作为开源硬件发布。因此，即使您对整个点击访问功能不感兴趣，您仍然可以构建一个样板闪存驱动器设计。我们以前没有见过很多解决 USB 大容量存储的 DIY 项目，也许这个设计可以改变这一点。

当然，前提是这东西能用。根据休息后的视频，[沃克]似乎在这次硬件改版中遇到了阻碍。当插入计算机时，它被列举为存储设备，操作系统声称其容量为零。他认为控制器和闪存芯片之间可能有交换的痕迹，所以希望他能在不久后解决问题。从夏天开始，我们就一直在关注这个项目，并渴望看到它跨越终点线。

 [https://www.youtube.com/embed/Wrcy6ySjSu8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wrcy6ySjSu8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



**编者按:**这与闪存盘本身无关，但让我们花点时间来欣赏一下[对所有用于制作项目的开源软件](https://youtu.be/Wrcy6ySjSu8?t=297)的开发人员的大声疾呼，以及【沃克】在演示结束时添加的配套视频。我们都应该记得向那些使我们的成就成为可能的人们表达敬意。