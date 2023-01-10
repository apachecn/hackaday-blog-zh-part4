# 简单的二进制手表使用 PCB 机身

> 原文：<https://hackaday.com/2022/07/21/simple-binary-watch-uses-a-pcb-body/>

有很多方法可以显示时间，从使用模拟表盘到 7 段显示。黑客们倾向于喜欢二进制手表，如果仅仅是因为他们与那些似乎能让世界转动的数字机器有联系的话。Vishal Soni 决定建造一个他们自己的。

这是一个简单的设计，用六位来显示时间。手表顶部的红灯亮起，表示手表正在显示分钟，这些分钟以二进制形式显示在下面的六个蓝色 led 上。然后，手表显示小时，并再次使用六个蓝色发光二极管显示相关数字。

[Vishal]将此称为二进制编码十进制(BCD)手表，但 BCD 涉及使用二进制直接指代 0-9 的数字。相反，它看起来是一个使用 6 位符号的常规二进制手表。

手表的核心是 ATtiny85，它还具有一个 TP4056，用于充电和维护为手表供电的锂电池。通过 USB-C 端口充电。这一切都是建立在一个定制的 PCB 上，它被设计成手表的主体，表带直接连接到 PCB 上。唯一缺少的是一个 32.768 KHz 的晶体或实时时钟，用于精确计时。

总的来说，这是一个有趣的构建，它教会了[Vishal]许多有用的设计技巧。我们想象这些将在未来的项目中很好地服务于[Vishal]。如果你正在挖掘二进制手表，考虑一下这些年来我们看到的一些[其他](https://hackaday.com/2020/05/03/binary-watch-looks-good/) [伟大的](https://hackaday.com/2018/07/24/a-bcd-wristwatch-youd-want-to-wear/) [建造](https://hackaday.com/2014/08/25/prove-your-geek-cred-with-a-binary-watch/)。休息后的视频。

 [https://www.youtube.com/embed/fd1oudY0hw8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1&wmode=transparent](https://www.youtube.com/embed/fd1oudY0hw8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1&wmode=transparent)

