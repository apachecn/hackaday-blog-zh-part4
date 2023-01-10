# 真正的联网 KVM，无需倾家荡产

> 原文：<https://hackaday.com/2020/11/24/true-networked-kvm-without-breaking-the-bank/>

为了同时管理多台计算机，IP KVM 是一种无价的设备，它使通过网络完成工作成为可能，而不必将键盘、显示器和鼠标拖到每台计算机上。唯一的缺点是它们可能会变得昂贵，当然，除非你能以比 Pi 本身的成本高一点的价格推出一个基于 Raspberry Pi 和 [PiKVM 镜像](https://pikvm.org/)的产品。

下面链接的视频显示了如何设置这一切，包括刷新图像，然后设置必要的硬件。该版本显示了一个通过 USB 使用 HDMI 的选项，但另一个使用 CSI 总线的选项将允许控制视频分辨率和颜色等选项，而 USB HDMI 加密狗不允许这样做。它还使重启计算机和配置 BIOS 或从可移动介质引导成为可能，这是像 VNC 这样的远程桌面解决方案不可能做到的。

PiKVM 的创建者[在之前关于 CSI 总线捕获卡](https://hackaday.com/2020/09/05/incredible-soldering-in-the-name-of-hardware-support/)的创建的帖子中提到过，基于这一构建的 Pi hat 将很快推出，其中也将包括 ATX 控件的选项。不过现在，你可以不用帽子就能自己构建所有这些，这也是 Pi-KVM 令人印象深刻的部分原因，同时它的成本也非常低。

 [https://www.youtube.com/embed/plP9Y1likRg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/plP9Y1likRg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

