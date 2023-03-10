# 入侵罗技 Z906 扬声器系统

> 原文：<https://hackaday.com/2022/05/19/hacking-the-logitech-z906-speaker-system/>

罗技 Z906 是一个全面的 5.1 环绕声系统。它能够输出 1000 瓦的峰值功率，并能如你所料解码杜比数字和 DTS 音轨。它旨在用作家庭影院系统的心脏，并与中央命令控制台一起使用。然而，[zarpli]发现了设备的序列秘密[，现在可以以独立的方式运行设备。](https://github.com/zarpli/Logitech-Z906)

事实证明，Z906 使用一个主控制台，通过 DE15 连接器(也称为 DB-15)与硬件的其余部分进行通信。[zarpli]意识到硬件可以被任何带有串口的设备控制。因此，一个可以很容易地与 Arduino 一起使用来控制 Z906 所有主要功能的库就诞生了。从音量到效果模式和通道分配，一切都可以由微控制器控制。作为压轴戏，【zarpli】展示了硬件在没有连接控制台的情况下演奏多声道乐曲[，而](https://www.youtube.com/watch?v=QVzbw9zAXnw)则用他自己的硬件来演奏。

如果你有一个罗技 Z906 或类似的单位，你希望自动化，你可能会发现这项工作很有用。对于任何考虑在其他硬件上的控制台端口上进行黑客攻击的人来说，这也是一个很好的灵感。休息后的视频。

 [https://www.youtube.com/embed/QVzbw9zAXnw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QVzbw9zAXnw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

