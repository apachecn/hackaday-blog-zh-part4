# 保持时钟准时，瑞士方式

> 原文：<https://hackaday.com/2019/09/17/keeping-clocks-on-time-the-swiss-way/>

对于一个有瑞士口音的人来说，还有比受制于一个秒针甚至是——恐怖的时钟更糟糕的命运吗？–偏离正确时间几分钟？的确不是，这就是为什么[【那个有瑞士口音的家伙】竭尽全力让他的宜家无线电控制时钟保持在正确的轨道上](https://www.youtube.com/watch?v=6SHGAEhnsYk)。

对于那些没有看过(安德烈亚斯·斯皮斯)YouTube 视频的人来说，你会知道他对瑞士人的刻板印象开了一点玩笑，比如精确和准时。但实际上，拥有一个应该与遍布全球的众多长波无线电原子钟之一同步的时钟，却无法做到这一点，即使是对时间最不痴迷的人也感到厌烦。他的宜家时钟应该可以读取来自德国 DCF77 站的信号，但即使是这种时钟中敏感的接收器也可能被地下场所击败，如[Andreas]的商店。他的解决方案是使用 Raspberry Pi 和向 GPIO 引脚发送调制时间信号的代码来提供 DCF77 的本地版本。pin 连接到铁氧体棒天线，这当然意味着 Pi 被变成了无线电发射机，因此可能违反了法律。但是正如安德烈亚斯指出的，如果能量保持足够低，辐射只会被附近的时钟接收到。

随着他的时钟现在通过微型电台安全地同步到 NTP 服务器上，【安德里亚斯】可以重新开始他的其他项目，例如[哈雷](https://hackaday.com/2018/07/18/harley-hardened-wire-helps-high-gain-antenna-hack/)天线的加工硬化铜线，或者[核启示录推特盖革计数器](https://hackaday.com/2017/10/08/connecting-a-50-geiger-counter/)。

 [https://www.youtube.com/embed/6SHGAEhnsYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6SHGAEhnsYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

