# 一个嘟嘟响的玩具帮助一只瞎狗玩捡东西游戏

> 原文：<https://hackaday.com/2020/12/12/a-beeping-toy-helps-a-blind-dog-play-fetch/>

当一只心爱的宠物失明了，并不意味着他们不能或不想再玩捡东西了，只是游戏必须有所改变。[Bud Bennett]的狗 Lucy 因渐进性肾萎缩慢慢失去了视力，但仍然可以玩玩具，所以[Bud]决定制作一个可以进入各种填充玩具的寻呼机，以帮助 Lucy 找到它们。露西不喜欢那些不停发出响声的商业玩具，尤其是当她把它含在嘴里的时候。

[![](img/8cb154029d92e384f014e934eb18cb3b.png)](https://hackaday.com/wp-content/uploads/2020/12/lucys-toy-guts.jpg) 这个微小的封装以 LIS3DH 加速度计为中心，用 PIC16F18313 编程。当玩具被抛向空中时，加速度计确定它处于自由落体状态，并触发 PIC 上的中断。压电蜂鸣器开始发出蜂鸣声，这样露西就可以找到它，然后过一会儿就停下来，等待下一次自由落体。功耗如此之低，以至于[Bud]预计大约每年为 120 mAh 的 LiPo 电池充电一次。

我们打赌[Bud]和 Lucy 之间的交流已经很好了，[但是也许她可以用一个狗的共鸣板更有表现力。](https://hackaday.com/2020/02/13/training-a-dog-to-speak-with-a-sound-board/)