# 用于业余无线电的 ATMega328 SSB SDR

> 原文：<https://hackaday.com/2020/05/27/atmega328-ssb-sdr-for-ham-radio/>

不起眼的 ATmega328 微控制器通常包装成 Arduino Uno，是数百万人进入电子和嵌入式编程世界的门户药物。有些人就是不能错过挑战，看看他们能把老黄牛推多远，看起来[Guido PE 1 NZ]就是其中之一。他已经成功地为 ATMega328 上的高频波段实现了一个软件定义的单边带业余无线电收发器[](https://github.com/threeme3/QCX-SSB)，看起来该项目正在取得进展。

这款收音机最初是一款 [QRP 实验室 QCX](https://hackaday.com/2017/09/13/a-fully-featured-fifty-dollar-qrp-radio/) 的产品，这是一款 49 美元的单波段连续波(莫尔斯电码)高频收发器套件，已经是使用高频波段最便宜的方式之一。[Guido]通过在 ATmega328 上实现大量数字信号处理，减少了约 50%的无线电器件数量。在发射机端，SSB 信号是通过使用 800kbit/s I2C 对 Si5351 时钟发生器进行轻微的频率改变，并使用 PWM 控制一个非常高效的 E 类 RF 功率放大器以获得约 5W 的输出功率来产生的。更高的效率意味着不再需要通常在单边带收音机上看到的笨重散热器。该无线电可在 80 米至 10 米(3.5 Mhz-30 Mhz)范围内连续调谐，但它需要为每个频段插入不同的低通滤波器。

改造后的 QCX 被命名为 QCX-SSB，但随着[圭多]和其他几个人的努力，该项目正在迅速发展，将它变成一个全新的收音机，称为 SDX。去 [讨论组](https://groups.io/g/ucx) 看看最新消息。如果你想构建自己的，目前最简单的方法是获得一个 QCX 工具包，并使用 QCX-SSB Github repo 上的说明来构建它。看看下面由[Manuel DL2MAN]撰写的概述。然而，该项目正在迅速发展，它似乎很可能很快就会超越其 QCX 基地和 ATmega328 供电。

这个项目可以大大降低新 ham 进入 HF 频段的技术和财务壁垒，我们肯定会密切关注它。如果你想只从接收机开始，看看这款基于硅实验室 Si4735 的 [多频带单边带接收机](https://hackaday.com/2020/03/02/multi-band-receiver-on-a-chip-controlled-by-arduino/) 。

 [https://www.youtube.com/embed/SRgaoK884tY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SRgaoK884tY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

