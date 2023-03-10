# 禁用英特尔在现代硬件上的后门

> 原文：<https://hackaday.com/2020/06/16/disable-intels-backdoor-on-modern-hardware/>

虽然英特尔管理引擎(以及类似程度的 AMD 平台安全处理器)继续以安全风险困扰着现代计算机处理器，但对于重视其所拥有的硬件和软件的安全性的用户来说，仍然取得了一些小小的进步。禁用 ME 的最新冒险是用于第八代和第九代英特尔芯片的 ASRock 主板。(还有一个[链接，链接到 Reddit 上关于这个项目的相关帖子](https://www.reddit.com/r/linuxhardware/comments/h90hu0/disabling_the_intel_management_engine_backdoor_on/))。

首先，简单回顾一下:ME 在 2008 年之前生产的一些计算机上是完全可移除的，在 2013 年前后生产的一些计算机上可以部分禁用或停用。对于我们这些想要现代硬件的人来说，这并不允许有很多选择，但由于各种各样的小“利用”，一些现代芯片组能够关闭 me。这是因为美国政府要求对敏感应用中的计算机禁用 ME，因此英特尔允许设置某个未记录的位，称为 HAP 位，以禁用 ME。研究人员已经能够在这个特定的主板上找到并操纵这个位来禁用 ME。

虽然这不会完全删除固件，但它确实以一种大型政府组织可以接受的方式停止了所有代码的执行，因此，如果您同时需要安全性*和*现代硬件，这是实现该目标的少数方法之一。还有其他[非常有限的选项](https://hackaday.com/2020/01/28/factory-laptop-with-ime-disabled/)，但如果你想完全删除 ME，即使是在旧硬件上，过程本身[并不像你想象的那样简单](https://hackaday.com/2016/12/16/installing-libreboot/)。

标题图片:来自柏林的 Fritzchens Fritz/[CC0](https://commons.wikimedia.org/wiki/File:Intel@180nm@P6@Coppermine@Pentium_III@unknow_Slot1_DSCx1_polysilicon_microscope_stitched@5x_(38025178422).jpg)