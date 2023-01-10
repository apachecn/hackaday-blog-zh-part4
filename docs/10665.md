# 逆向工程一个非常便宜的健身带

> 原文：<https://hackaday.com/2021/07/08/reverse-engineering-a-very-cheap-fitness-band/>

随着大牌智能手表在市场上的崛起，也有少量低端产品。M6 健身乐队就是其中之一，[和【Raphael】着手用自己创作的定制固件来破解这款廉价设备。](https://rbaron.net/blog/2021/07/06/Reverse-engineering-the-M6-smart-fitness-band.html)

售价约为 6 美元的 M6 手环似乎与更贵的(～50 美元)小米 Mi Smart Band 6 健身追踪器在名称上相似。经过反汇编，【Raphael】发现运行该节目的片上系统是一款 Telink TLSR8232。它配有一个 160×80 的显示屏，一个小型脂肪电池，一个振动马达和一个看起来像是假的心率传感器。

[Raphael]想要用新的固件来刷新 SOC，并从[atc1441]创建的类似部件[的代码中学到了很多东西。花了一些时间才弄清楚如何使用有点古怪的 SWire 接口给芯片编程，但[Raphael]坚持不懈，经过大量研究和实验，最终让事情运转起来。](https://github.com/atc1441/ATC_MiThermometer)

从那时起，还需要做进一步的工作来弄清楚如何读取电容按钮输入以及如何驱动屏幕，但[拉斐尔]最终成功了。最终的结果是快速制作了一个固件，允许他读取安装在家中植物上的蓝牙低能耗土壤湿度传感器。

这不是[拉斐尔]，又名[巴隆]的第一口樱桃；[在](https://hackaday.com/2018/05/29/hacking-a-fitness-tracker/)之前，我们已经报道过他在破解类似健身乐队方面的努力！休息后的视频。

> 为了绘制文本，我借用了 Picopixel 位图字体，并编写了一点文本渲染函数。所以我们可以欣赏这部电影杰作。[pic.twitter.com/0KqR0RPPt7](https://t.co/0KqR0RPPt7)
> 
> —拉斐尔(@ r baron _)[2021 年 7 月 6 日](https://twitter.com/rbaron_/status/1412454588242878467?ref_src=twsrc%5Etfw)