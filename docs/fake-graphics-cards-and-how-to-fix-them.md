# 假显卡及如何修复

> 原文：<https://hackaday.com/2019/08/02/fake-graphics-cards-and-how-to-fix-them/>

在网上购物时，现代图形硬件有很多优惠。当然，如果你像[Dawid]一样，花 48 美元从 Wish 买了一台 GTX1050 Ti，你大概会怀疑这好得不像真的。当然，你是对的。

[Dawid]从一开始就注意到卡片的包装与众不同。虽然它被 NVIDIA 和 GeForce 品牌所覆盖，但没有型号或总体系列的说明。该卡松散地包装在泡沫塑料包装中，在运输过程中可以自由弹跳。安装后，该卡报告自己是 GTX1050 Ti，但拒绝与 NVIDIA 驱动程序正常工作，并经常导致蓝屏死亡。

拆开后，很明显，该卡只是一个制造不良的 GTS450 修订版 2，比其宣传的卡老了五代以上。由于实际硬件和卡报告的不匹配，驱动程序无法正常使用卡。

对于那些被骗的人来说，还有一些希望。[Phil]有过使用这些卡的经历，这些卡同样错误地报告了它们的实际硬件。为了纠正这一点，这些卡需要刷新其 BIOS 以反映现实，但这些假卡无法与 NVIDIA 的 NVFlash 工具一起工作。相反，它们必须使用 EEPROM 编程器手动刷新。一旦这些卡被闪存了适当的 BIOS，它们就可以与适当的驱动程序一起使用，并正常工作，尽管其性能比宣传的要差得多。

这是对在线购物平台状态的一个有趣的洞察，古老的格言仍然是正确的——如果它好得令人难以置信，它可能是真的。另外，[黑掉 GPU 往往能有很大的成果](https://hackaday.com/2013/03/18/hack-removes-firmware-crippling-from-nvidia-graphics-card/)。休息后的视频。

 [https://www.youtube.com/embed/Ra0T0j5KoAc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ra0T0j5KoAc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/wrVff6C1das?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wrVff6C1das?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

