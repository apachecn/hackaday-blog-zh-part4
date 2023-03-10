# 不是你的普通数码管时钟

> 原文：<https://hackaday.com/2021/11/09/not-your-average-nixie-tube-clock/>

当谈到谢妮时钟时，我们都非常清楚会发生什么:一堆下面有一些 RGB LEDs 的 Nixies，某种类型的木箱，也许还有一些黄铜齿轮或配件，以实现真正的蒸汽朋克外观。这并不是说我们不欣赏这些建筑，但有时趋同设计可能有点多。谢天谢地，这个 60 管的谢妮钟很大程度上符合这种模式。

[limpkin]设计的关键是 IN-9 谢妮，这是一个细长的管子，过去常常显示为线性指示器；想想台式万用表上显示的条形图或混合板上的 VU 表。[limpkin]意识到试管上的 60 可以放射状排列来代表小时或分钟，甚至更多。IN-9 中亮起的段的长度由通过灯管的电流控制，因此[limpkin]为每个段设计了一个简单的驱动器，将 PWM 信号作为其输入。60 通道、14 位 PWM 控制器的工作落到了 FPGA 身上。ESP8266——五年前当他[开始项目](https://hackaday.com/2016/04/13/powering-a-lot-of-nixie-tubes/)时风靡一时——负责计时和控制，以及驱动钟面中心四个 7 段 led 的更传统的时钟显示。

定制的 PCB 位于 CNC 加工的 MDF 木材表面；IN-9 通过面部的缝隙发光，而七段显示器通过变薄的区域显示。它看起来很酷，有很多显示选项，就像下面视频中显示的音频摄谱仪。我们很高兴[limpkin]在这么久之后决定分享这个。

 [https://www.youtube.com/embed/4m_zUL-QL6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4m_zUL-QL6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

