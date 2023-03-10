# 人造牛在人造房间里咀嚼人造草

> 原文：<https://hackaday.com/2019/10/24/faux-cow-munches-faux-grass-on-a-faux-roomba/>

在农村，养一头或两头奶牛没什么大不了的。你可以有一个装满他们的牛棚，没有人会眨一下眼睛。但是如果你住在大城市，不需要宠物狗或宠物猫，但是需要一只宠物牛，那该怎么办呢？让它乘坐电梯并不容易，而且你很有可能在附近非常非常不受欢迎。[戴恩&妮可]，又名[8 比特和一个字节]却毫不气馁，并建立了[Moomba-奶牛 Roomba](https://www.hackster.io/8bitsandabyte/mooomba-the-cow-roomba-be3a52)在他们的小城市公寓里陪伴他们。

主平台是由几块木材建成的，因为它需要看起来像一个 Roomba，切割成圆形。动力来自两个 DC 齿轮电机和第三个自由旋转的轮子，它们都直接连接在木制框架上。马达从八节“AA”电池获得 12V 电力。自由放养的牛也需要一些智慧来让它随意漫游。为此，它使用了一个由电源供电的树莓 Pi。Pi 驱动一个双通道继电器板，控制施加到两个电机上的电压。不幸的是，这阻止了 Moomba 在陷入死胡同时退出。对于任何试图建立这一点的人来说，应该很容易用电子速度控制器或甚至通过添加第二个双通道继电器板来修复，该继电器板可以反转施加到电机的电压。Moomba 需要“哞哞”地叫，所以 Raspberry Pi 将预先录制的 mp3 音频片段传输到一对 USB 扬声器。

如果你在休息后看到视频，你会注意到让 Moomba 有感觉是一件简单的事情，只需做“ctrl+C”和“ctrl+V ”,你就可以开始了。python 代码是直接的，做四个动作之一——向前移动、左转、右转或播放音频。该代码从 0 到 3 中选取一个随机数，然后执行与该数字相关的操作。最后，作为一个额外的奖励，Moomba 得到了一片茂盛的人造绿草，它可以自由地在牧场上漫步。

乍一看，许多人可能会讽刺说“黑客在哪里”？但是像这样简单、容易执行的项目非常适合让年轻人在成人的监督下开始学习黑客。最终的结果可能看起来很无聊，但它会让年轻的心灵兴奋不已，因为他们从观看中学习。

 [https://www.youtube.com/embed/1YdVM4I5srY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1YdVM4I5srY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

