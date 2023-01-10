# 揭开 Echo Dot 隐藏的 USB 端口

> 原文：<https://hackaday.com/2019/08/15/uncovering-the-echo-dots-hidden-usb-port/>

如果你升级到亚马逊最新的 Echo Dot，你可能会惊讶地发现这个小巧的语音助手已经去掉了 USB 端口。早期型号的 Dot 使用普通的微型 USB 端口供电，黑客最终发现这也为窥探设备的固件提供了一种有用的方法。在最新的 Echo Dot 上，USB 端口被删除，取而代之的是一个简单的桶形电源连接器，这一事实被一些人视为亚马逊试图让好奇的所有者远离他们的硬件的迹象。

但是正如布莱恩·多雷所展示的，他们所做的只是在道路上加了一个凸起。虽然他们移除了外部 USB 连接器，[它的轨迹仍然在板上等待被访问](https://www.briandorey.com/post/echo-dot-3rd-gen-digging-deeper)。更好的是，原来 USB 数据线连接到位于圆点底部的测试点。你只需要一个简单的插座，通过设备外壳上现有的开口连接，你就可以拿回你的 USB 端口了。

那么你能用 USB 在 Echo Dot 上做什么呢？嗯，现在不多。【Brian】发现圆点显示为使用`lsusb`的 Linux 下的联发科设备，`fastboot`可以看到它，甚至确认锁定的 bootloader 的存在。社区需要做一些工作来看看这个特殊的兔子洞有多深。

即使你对恢复它的 USB 端口不感兴趣，[Brian]在他的深入研究中发现了大量关于 Echo Dot 的有趣的硬件信息。他绘制了位于设备 PCB 上的许多测试点，并发现了一些值得进一步研究的有趣点。例如，他发现将其中一个引脚拉高会触发 Dot 使其麦克风静音；这对任何想盖住 Alexa 耳朵的人来说都很有用。

上个月[Brian]第一次打开了 Echo Dot，在亚马逊的 Prime Day 销售期间，他以低价获得了一个。看起来他在揭开这个流行小玩意的神秘面纱方面取得了相当快的进展，[我们非常想知道这项研究将把我们带向何方](https://hackaday.com/2017/08/03/the-amazon-echo-as-a-listening-device/)。