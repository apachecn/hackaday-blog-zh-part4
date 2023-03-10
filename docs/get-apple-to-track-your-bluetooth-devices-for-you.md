# 让 Apple 为您跟踪您的蓝牙设备

> 原文：<https://hackaday.com/2021/03/05/get-apple-to-track-your-bluetooth-devices-for-you/>

苹果公司的“查找我的”服务允许用户通过利用一个全球网络的位置感知网关来跟踪他们丢失的设备。随着数以百万计的 iPhones 和 MAC 在野外监听失踪设备的蓝牙广告，并将他们的发现转发给库比蒂诺的母舰，只要硬件留在相对城市化的地区，这是一种非常有效的跟踪硬件的方法。不幸的是，该系统完全是专有的，非苹果设备不被邀请参加。

或者至少，过去是这样。[安全移动网络实验室最近发布的一个名为 OpenHaystack](https://github.com/seemoo-lab/openhaystack) 的项目展示了通用设备如何通过模仿适当的蓝牙低能量(BLE)广播来利用苹果的 Find My network。目前，他们有一个 BBC micro:bit 的固件映像，以及一个 Linux 的 Python 脚本，这将允许你即兴创建一个 Find My target。但该团队也发布了在其他支持 BLE 的设备和微控制器上实现类似功能所需的所有信息，因此预计支持的硬件列表将很快增长。

![Diagram showing how the Apple Find My system works](img/09f3cb155a4f02901ea2104a495d6c88.png)有点讽刺的是，虽然 OpenHaystack 允许你在 Find Me 跟踪网络上跟踪非苹果设备，但你*将*需要一台 Mac 电脑来实际查看你的设备在哪里。该团队的软件需要运行 macOS 11 (Big Sur)的计算机才能运行，根据它与 Apple Mail 集成以通过私有 API 提取跟踪数据的事实来判断，我们将假设这不是可以以平台无关的方式轻松重现的东西。[除了偶尔会有黑客潜入](https://hackaday.com/2015/02/07/hackintosh-project-looks-like-a-mac-smells-like-a-mac/)，看起来蒂姆·库克可能会笑到最后。

目前还不清楚苹果填补这个漏洞会有多困难，但利用私有 API 的说法让我们认为，这个项目的可行性可能会有一个内置的时间限制。毕竟，[大型科技公司通常不赞成我们这些小工长时间窥探他们的阴谋诡计。尽管苹果找到了阻止 OpenHaystack 的方法，但预计该公司将在今年的某个时候发布“空中标签”，允许用户通过该系统跟踪他们喜欢的任何对象。](https://hackaday.com/2021/01/26/whats-the-deal-with-chromium-on-linux-google-at-odds-with-package-maintainers/)