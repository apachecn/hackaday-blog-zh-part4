# 射频烧伤和爆炸的电脑扬声器:Sophos 看证据

> 原文：<https://hackaday.com/2021/06/21/rf-burns-and-exploding-pc-speakers-sophos-looks-at-the-evidence/>

每年六月，一个不太可能叫[R.F. Burns]的人会在 Linux 内核邮件列表上发布一个问题，询问是否有可能出现一个让 PC 扬声器爆炸的 Linux 内核模块。这显然是一个玩笑，这也是为什么英国反病毒公司 Sophos [专门为此写了一篇轻松的博客文章。](https://nakedsecurity.sophos.com/2021/06/18/can-you-blow-a-pc-speaker-using-only-a-linux-kernel-driver/)

这篇文章是对早期 PC 声音的有趣转变，当时唯一保证存在的硬件是一个连接到输出端口的小扬声器。该位可以循环发出方波蜂鸣声，或者通过许多巧妙的操作可以发出低比特率的 PWM，发出几乎可以理解的声音，包括音乐和语音。他们的结论是，由于扬声器将被设计为始终处于 5 伏输出位的最大幅度，因此不可能通过软件将其破坏，我们倾向于同意这一点。有一种微小的可能性，一些扬声器可能有一个可以在软件中找到的共振频率，但我们并不完全相信。

你的黑客抄写员可能已经在大学的计算机实验室里花了一段时间，试图编写 C 代码，在 XT 扬声器上产生可用的 PWM，但失败了，但那些记忆力强的人可能会想起用于 Windows 3.1 的 PC 扬声器驱动程序。如果你是 chiptune 音乐的粉丝，甚至有为这种最基本的乐器创作的[整张专辑。](https://hackaday.com/2019/02/23/the-pc-speaker-lives-on-as-a-new-album/)

头图:MKFI，[公共域](https://commons.wikimedia.org/wiki/File:PC_speaker.JPG)。