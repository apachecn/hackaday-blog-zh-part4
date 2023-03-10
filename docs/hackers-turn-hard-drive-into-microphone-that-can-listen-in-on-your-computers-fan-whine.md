# 黑客将硬盘变成麦克风，可以监听计算机风扇的呜呜声

> 原文：<https://hackaday.com/2019/03/13/hackers-turn-hard-drive-into-microphone-that-can-listen-in-on-your-computers-fan-whine/>

据 [The Register](https://www.theregister.co.uk/2019/03/07/hard_drive_eavesdropping/) 报道，黑客现在可以通过把硬盘变成麦克风来监听你电脑周围的对话。需要注意的是:只有当这些对话的声音是搅拌机的两倍，或者大约是割草机的声音时，黑客才起作用。总之，没人说话那么大声，往前走，这里没什么好看的。

该攻击将在 2019 年 IEEE 安全和隐私研讨会上提出，并将该攻击描述为对磁盘驱动器上的固件进行修改，以读取位置误差信号，从而将读/写头保持在最佳位置。这个 PES 受气压影响，如果有什么东西受气压影响，你就有一个麦克风。在这种情况下，这是一个可怕的麦克风，它机械地耦合到一台有很多振动的机器上，包括旋转的盘片和计算机内部的一堆风扇。这是一个学术练习，而不是真正的攻击，无论哪种方式来泄漏这些数据，您都需要找到硬盘所连接的计算机。它一路向下攻击。

这种攻击的限制因素是，它需要在硬盘附近进行*非常大声的*对话。为了录制语音，研究人员不得不将音量提高到 85 dBA，大约相当于搅拌机粉碎冰块的音量。通过这个麦克风录制音乐以便 Shazam 可以识别音轨意味着以 90 dBA 的音量播放音轨，或者说与割草机的音量相当。基本上，这是不可能的。

这个黑客有趣的一点不是把硬盘当作麦克风。它正在修改硬盘上的固件来做一些事情。[在](http://spritesmods.com/?art=hddhack)之前，我们已经见过一些类似的黑客攻击，但是关于硬盘固件黑客攻击的最新公开文献已经是好几年前的事了。如果你有破解硬盘的建议，即使是做一些非常不切实际的事情，我们也很乐意看到。