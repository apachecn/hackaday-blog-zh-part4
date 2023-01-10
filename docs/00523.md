# 对高功率闪光灯和嗡嗡声的追求

> 原文：<https://hackaday.com/2018/09/03/the-quest-for-high-powered-blinky-and-buzzing/>

有时，我们需要设备来通知我们一些事情。烤箱计时器开始计时了。你的手机有推送通知。烟雾探测器电池电量越来越低。所有这些问题都可以通过蜂鸣器或 LED 来解决。这是一个简单而容易解决的问题。

但是，如果你需要知道一台柴油发动机是否出了问题，发出 90 分贝的噪音，该怎么办呢？如果不能保证你就在发动机旁边呢？如果你需要告诉半英里内的每个人有什么不对劲呢？同样，发光二极管和蜂鸣器，但标准的，现成的实施是不会削减它。你需要大量的蜂鸣器和发光二极管，你需要用相当高的电流来驱动它们。你如何解决这个问题？

这是[Tegwyn] [为他的另一个 Hackaday 奖参赛作品](https://hackaday.io/project/114107-mega-powerful-flashy-beeper-module)必须解决的问题。解决方案是你所期望的——蜂鸣器和发光二极管——但是他在这些设备后面放了一些严重的电流。事实上，当你按这么多蜂鸣器的时候，要考虑热量因素。

这个项目的发光二极管是一些耀眼的 1209 和 1206 SMD 部件，蜂鸣器是一个令人讨厌的响亮的 SMD 97 dB 蜂鸣器。这块板上有八个蜂鸣器。那么，如何驱动这些耗电设备呢？[Tegwyn]使用 L293E 半桥电机驱动器，采用“功率下降”封装，散热效果相对较好。有用吗？哦，是的，而且很讨厌。看看下面的视频，自己判断。事实上，你可以通过增加更多的能量来让一些东西变得更响更烦人。

 [https://www.youtube.com/embed/yksx4jS9eaw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yksx4jS9eaw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)