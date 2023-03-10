# PCB 上的特斯拉线圈

> 原文：<https://hackaday.com/2019/04/25/a-tesla-coil-from-pcbs/>

二月份在荷兰的 Hacker Hotel 营地，我们的注意力被转移到了一个不寻常的项目上。[Niklas Fauth]买了一个特斯拉线圈，但它不是普通的特斯拉线圈。它没有采用通常的高线圈和甜甜圈形状的电容帽，而是采用了一堆印刷电路板的形式，它们之间有间隔，因为特斯拉线圈只是简单地*更酷*这样，他让它作为一个即兴的 MIDI 驱动等离子球扬声器播放音乐。现在他已经能够写下这个项目，我们可以更仔细地看看，它不仅对双共振特斯拉线圈，而且对氮化镓晶体管进行了引人入胜的介绍。

特斯拉线圈的限制因素来自晶体管在较高频率下有效开关的能力。很少有设计能超过几十 kHz 的开关频率，因此它们依赖于我们习惯的大线圈。对于这些较低的频率，PCB 线圈实际上没有足够的电感，因此 Niklas 的设计采用了非常高的频率，实际上对于 Tesla 线圈设计来说是 2.6 MHz，初级和次级线圈都是谐振的。他的文章详细阐述了传统 MOSFETS 和双极性晶体管在该应用中的缺点，并阐述了他在使用 GaN FETs 时的设计选择。他正在使用的设备是 TI LMG5200 GaN 半桥驱动器，它包括产生 GaN FET 苛刻驱动要求的所有必要电路。

设计文件可以在 GitHub 库中找到，你可以在下面的视频中看到他们三人的合唱。同时[Niklas]是一个多产的硬件黑客，他的作品过去曾出现在这些页面上，所以看看他的[超声波相控阵](https://hackaday.com/2018/08/19/the-engineering-of-an-ultrasonic-phased-array/)和他的 [x 射线图像传感器作品](https://hackaday.com/2018/03/15/reverse-engineer-an-x-ray-image-sensor/)。

 [https://www.youtube.com/embed/6EcucigRQ4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6EcucigRQ4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)