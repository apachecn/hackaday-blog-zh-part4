# 研究极简 LED 灯中的新芯片

> 原文：<https://hackaday.com/2021/05/27/investigating-a-new-chip-in-a-minimalist-led-lamp/>

拆卸廉价电子设备可能会产生有趣或恐怖的结果，或者两者兼而有之，尤其是在涉及市电电源的时候。[bigclivedotcom]对一种极简 LED 灯进行了逆向工程处理，并发现了一种新的芯片，只需要四个额外的无源元件就可以在交流电源上运行 LED。

问题中的芯片是 1981 年的乔瓦特·JWB，互联网上没有关于它的数据表。但是，JW1981 有一个数据手册，它是一个线性 LED 驱动器。在对 PCB 进行逆向工程后，[bigclivedotcom]得出结论，JW**B**1981 必须包括板载桥式整流器。板上仅有的其它元件是三个电阻、一个电容和 led。第一个电阻限制流入大平滑电容的浪涌电流。第二个电阻用于电容放电，而最后一个电阻设置调节器的电流输出。

像其他 LED 电路一样，可以取消平滑电容器和放电电阻器，这也使光线变暗。然而，这导致 led 在交流频率下非常令人讨厌的闪烁，尤其是在低亮度设置下。

与往常一样，这是一个来自[bigclivedotcom]的信息丰富的视频，它是基于一位观众发送的一张 PCB 图片完成的。他还提到，通过将电流设定电阻器换成更大的电阻器，灯的寿命可能会增加。

我们已经报道了几个【bigclivedotcom】的视频，涉及的话题从[自供电无线开关](https://hackaday.com/2021/05/02/reverse-engineering-self-powered-wireless-switches/)到[用电解液填充假电容](https://hackaday.com/2019/10/23/top-off-a-dry-electrolytic/)。

 [https://www.youtube.com/embed/toXaBxp1It8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/toXaBxp1It8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

