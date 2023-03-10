# 随着节拍擦拭你的挡风玻璃

> 原文：<https://hackaday.com/2019/10/24/wiping-your-windscreen-to-the-beat/>

没有什么比你的挡风玻璃雨刷在节奏下降时感觉不到更破坏你的心情了。每个主要的汽车制造商都专注于为大众制造电动自动驾驶汽车，却忽略了这个非常现实的问题。好吧[伊恩·查纳斯]接管了，并成功地控制了他汽车的雨刷，使之与立体声音响合拍。

从基础开始，[Ian]首先需要控制雨刷马达的速度。这是使用从另一个项目改编的定制电源完成的。该系统的大脑是一个树莓派 3B+,它运行一个锁相环算法来同步音乐和电机。检测节拍被证明是这个项目中最困难的部分，根据[Ian]所做的研究，没有标准的解决方案。他最终选择了“ [madmom](https://github.com/CPJKU/madmom) ”，这是一个 Python 音频和音乐信号处理库，它运行一个神经网络来实时检测节拍。Raspi 通过串行向 Arduino 发送所需的 PWM 和使能信号，Arduino 进而控制电源。整个系统被巧妙地集成在汽车中，仪表板上有一个开关，可以根据需要将电机连接到新的电源，使雨刷仍然可以正常(安全)使用。

伊恩为这个想法提交了临时专利申请，并将很快在易贝的[拍卖会上进行](https://www.iancharnas.com/dancing-wipers/)拍卖，希望一些主要的汽车制造商会感兴趣。对于老爷车，你可以[把一个 Arduino 塞进音响](https://hackaday.com/2017/06/04/a-retro-car-stereo-with-arduino-inside/)，或者做一个[超级便宜的蓝牙升级](https://hackaday.com/2014/12/01/15-car-stereo-bluetooth-upgrade/)。休息之后请看视频。

 [https://www.youtube.com/embed/oJkZpBi6n6Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oJkZpBi6n6Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

