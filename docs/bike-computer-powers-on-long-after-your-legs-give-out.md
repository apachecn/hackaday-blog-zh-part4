# 自行车电脑在你的腿筋疲力尽后还能长时间工作

> 原文：<https://hackaday.com/2020/08/20/bike-computer-powers-on-long-after-your-legs-give-out/>

商店货架上的典型自行车电脑会显示你的速度、行程距离、里程表，也许还有时间。我们可以从磁传感器和时钟中获得所有这些数据，但我们生活在一个有各种传感器可供我们使用的世界中。[马蒂亚斯·n .]有动力将其中一些放入一台整洁但功能强大的自行车电脑中，这台电脑有指南针、温度和气压。

大脑是一个 STM32L476 低功耗控制器，还有一个清晰的内存 LCD 显示器，因为它是快速刷新率和低功耗之间的一个很好的妥协。对于户外可读性来说，电子纸是一个不错的选择(显然也是低功耗的),但没有比一个落后的速度表或指南针更糟糕的了。

出于一种自我克制，他没有尝试更换手机，所以没有 GPS，WiFi，或流媒体音乐。与他值得信赖的手机不同，你测量电池的寿命是以周为单位的。他实现了 EEPROM 存储器，通过电源循环来保存持久数据，防水板包括电池充电电路，便于在骑行之间充电。

当你把手机的能量扔向自行车电脑时，有人会揭开安卓系统的面纱，或者你可以通过你的踏板测量不同的能量。

 [https://www.youtube.com/embed/f_nbbbMXRL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f_nbbbMXRL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)