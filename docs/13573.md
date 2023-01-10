# 作为非车载显示适配器的 Raspberry Pi

> 原文：<https://hackaday.com/2022/05/09/a-raspberry-pi-as-an-offboard-display-adapter/>

与它的 USB 祖先相比，不起眼的 USB-C 端口给我们带来了如此多的优势，其中之一是作为笔记本电脑的便捷显示输出。只需添加一个便宜的适配器，就可以连接从手机到 HDMI 显示器或投影仪的任何东西。但有一个障碍，仅仅有 USB-C 是不够的，因为设备必须支持显示功能。这是[Gunnar Wolf]在使用联想 ARM 笔记本电脑时不得不面对的问题，他的解决方案出人意料。他用的不是适配器，而是树莓 Pi 3 和一些软件技巧。

一个显而易见的非机载 Pi 镜像机载视频的路线是使用 VNC，他尝试过，但发现由于滞后而有所欠缺。作为 Wayland compositor 的用户，他发现他可以使用 [wf-recorder](https://github.com/ammen99/wf-recorder) 并将其输出发送到流，从而以 Pi 可以通过网络读取的方式捕获他的屏幕。这不是一个像纯硬件适配器那样方便的解决方案，但至少它允许他共享屏幕。

令人惊讶的是，我们经常发现项目需要使用现有的硬件来镜像计算机的显示，至少[这个比其他一些](https://hackaday.com/2016/10/24/when-your-screen-breaks-in-the-himalayas/)更优雅。