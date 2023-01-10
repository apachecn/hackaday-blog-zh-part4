# LED 窃听

> 原文：<https://hackaday.com/2021/08/25/eavesdropping-by-led/>

如果你感觉有人在看你，也许他们也在听。由于一种叫做“[萤火虫](https://www.nassiben.com/glowworm-attack)的新攻击，至少他们可能会听到你电脑扬声器里传来的声音在这个新的攻击中，仔细观察扬声器上的电源 LED，攻击者可以重现播放的声音，这要归功于 LED 亮度几乎察觉不到的波动，很可能是由于扬声器的电源线下垂和恢复。

你可能会认为，如果你能看到 LED，你只能听到扬声器的输出，但通过一个 100 英尺远的窗口望远镜似乎就足够了。你可以想象，从远处一个嘈杂的办公室里，你也可以玩同样的把戏。我们不知道——但我们怀疑——即使耳机插入扬声器，LED 仍然会调节音频。任何为扬声器供电的设备都是潜在的泄漏源。

一方面，这是阴险的，因为与更积极的窃听形式不同，这几乎是无法察觉的。另一方面，也有各种低技术和高技术的攻击缓解措施。低科技？关上百叶窗或用胶带盖住 LED。高科技？给 LED 输入一个随机频率来破坏任何泄露的信息。超级间谍技术？把假的扬声器放在真的扬声器前面，这些扬声器会无声地播放 led 上的错误信息。

该视频播放了恢复的语音样本，老实说，它足够清晰，但不是很好。我们想知道一些额外的信号处理是否会有所帮助。

[被动 bug](https://hackaday.com/2015/12/08/theremins-bug/)很难发现。即使是一个奇特的[结检测器](https://hackaday.com/2017/09/20/spy-tech-nonlinear-junction-detectors/)也不会告诉你你的扬声器是否受到了萤火虫的攻击。

 [https://www.youtube.com/embed/z4-OFLTHtiw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=3&wmode=transparent](https://www.youtube.com/embed/z4-OFLTHtiw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=3&wmode=transparent)

