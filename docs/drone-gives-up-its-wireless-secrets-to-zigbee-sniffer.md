# 无人机将其无线秘密交给 Zigbee 嗅探器

> 原文：<https://hackaday.com/2019/02/08/drone-gives-up-its-wireless-secrets-to-zigbee-sniffer/>

解码一个未知的通信协议有些令人兴奋。您从一些线索开始，用一些简单的工具解决问题，最终找到第一个让您破解代码的突破口。这可能会令人沮丧，但当你最终获胜时，这可能是非常有益的。

似乎[Jason]在解码他的大众市场四轴飞行器和控制器之间的无线对话时了解到了这一点。问题中的 quad 是 Yuneec Q500，是一种中档、随时可以飞行的无人机，目标是那些希望轻松进入空中并拍摄一些很酷的照片的人。不知道无人机和控制器是如何交谈的，[杰森]打开盖子，发现里面有一个 Zigbee 芯片组。在一个 14 美元的 Zigbee USB 加密狗和 TI 的一些数据包嗅探软件的帮助下，[Jason]能够看到数据包流动，但解码它们是很费力的。幸运的是，sniffer 应用程序可以设置为将数据包传输到另一个设备，因此[Jason]编写了一个程序来接收和显示数据包。他用它来完整地描述每个控制器输入和从无人机返回的数据。这是一个漫长而奇怪的工具链，但结果是他现在能够实时创建 KML，并在谷歌地球上跟踪无人机的飞行。下面的视频显示了建设和一些后院试飞。

祝贺[杰森]打破协议，为其他黑客开放了这样的无人机。如果你有兴趣学习更多关于 Zigbee 嗅探的知识，你实际上可以将一些智能家居小工具变成有用的嗅探器。

 [https://www.youtube.com/embed/8kcNr7W3Dmk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8kcNr7W3Dmk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

