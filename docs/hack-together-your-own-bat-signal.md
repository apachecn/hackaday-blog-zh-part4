# 黑进你自己的蝙蝠信号

> 原文：<https://hackaday.com/2020/07/11/hack-together-your-own-bat-signal/>

蝙蝠利用回声定位来观察前方的物体。它们发射大约 20 千赫(最高 100 千赫)的超声波脉冲，然后在脉冲从物体反射回蝙蝠时感应到脉冲。这和超声波近程传感器用于物体规避的机制是一样的。人类(可能除了非常年轻的人)听不到超声波脉冲，因为频率太高，但简单的蝙蝠探测器中的廉价麦克风可以听到。事实证明，蝙蝠探测器是现成的，但这有什么意思呢？所以，像任何优秀的黑客一样，[威尔科尔] [决定打造自己的](https://www.instructables.com/id/Bat-Detector/)。

[WilkoL 的]设计主要由驻极体麦克风、麦克风前置放大器、CD4040 二进制计数器、LM386 音频放大器和扬声器组成。音频信号是模拟信号，其幅度根据声音与麦克风的距离而变化。[WilkoL]想要尽可能远地拾取蝙蝠的声音，所以他将麦克风前置放大器的增益调高了不少，实质上是控制了放大器。因为他主要关心声音的频率而不是振幅，所以他不关心晶体管输出的饱和。

CD4040 然后将信号除以 16，产生人耳可听频率范围内的输出信号。20 kHz 的 bat 信号分频至 1.25 kHz，最高 100 kHz 的 bat 信号分频至 6.25 kHz。

他能够用超声波测距仪和叮当作响的钥匙链产生的噪音来测试他的蝙蝠探测器(显然叮当作响的钥匙中有一些非常不可闻的高频成分)。他还没能得到他的设备捕捉蝙蝠的记录。它已经在很多场合探测到了蝙蝠，但是他太晚了一点没有拍到它。

无论如何，我们绝对期待看到蝙蝠探测器的行动！谁知道呢，[也许他会找到蝙蝠侠](https://hackaday.com/2011/02/14/batman-inspired-hidden-light-switch/)。

 [https://www.youtube.com/embed/xESE4mBGucI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xESE4mBGucI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

