# 音频合成的瑞士军刀

> 原文：<https://hackaday.com/2018/10/31/the-swiss-army-knife-of-audio-synthesis/>

30 年前，如果电脑能播放音频，我们就已经很幸运了。拿一台 20 年前的电脑来说，如果它能实时播放 MP3，你就很幸运了。现在，计算机可以处理数百首 CD 质量的音频，微控制器比 90 年代中期的台式计算机强大几倍。这意味着，当然，微控制器可以做音频非常，非常好。为了获得黑客日奖，[杨奇煜]利用这种力量创造了一把音频合成的瑞士军刀。它被称为噪音块(Noise Nugget)，当你想把音频放入*任何东西时，这正是你所需要的。*

问题中的微控制器是运行在 180MHz 的 ARM Cortex-M4，具有高质量的 DAC。有 USB、两个音频输出、一个音频输入、I2C、UART 和 GPIOs 形式的连接。有了这个，你就有了一个带 MIDI 接口的数字合成器，吉他踏板胡闹的音频效果，一个播放预录声音的音频效果触发板，一个数字录音机和一个 USB 声音接口。

那么，有了这些处理能力，噪声块实际上能做什么呢？嗯，首先，它是一个采样器。[杨奇煜]有一个在采样器模式下设置的噪音块的视频演示，它可以播放类似鲁特琴的样本和猫的声音。所有这些都通过 MIDI 控制，并通过一个便宜的扬声器播放。结果——除了猫的样本——听起来不错。你可以看看下面的视频。

 [https://www.youtube.com/embed/qIOF_VmpMX4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qIOF_VmpMX4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)