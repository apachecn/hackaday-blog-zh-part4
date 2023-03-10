# 旋转式电话 MIDI 控制器仍然可以打电话

> 原文：<https://hackaday.com/2022/03/15/rotary-phone-midi-controller-still-makes-calls/>

[Kevin]早就想用老式旋转手机和 Arduino 做些音乐，他终于这样做了[，并在五集系列节目](https://diyelectromusic.wordpress.com/2022/03/10/vintage-rotary-phone-midi-controller/)中首次尝试了 HTML。他发现了一个不错的旧英国电信号码，但它已经被转换成插头和插座布线，以适应现代系统。正因为如此，[凯文]希望保持它作为一部手机的完整功能。毕竟，在 2025 年之前，它应该还能正常工作，到那时，[凯文]所在的地区将不再支持脉冲拨号。

[![](img/55131261d0f8c08bdf17e695c52f7541.png)](https://hackaday.com/wp-content/uploads/2022/03/rotary-MIDI-inner.png) 正如你可能理解的那样，[凯文]热衷于从外部与手机进行交互，而不接触手机内部。他使用一个牺牲 ADSL 滤波器的 PCB 断开插座，并在引脚和 5 V 之间添加一个上拉电阻。

[Kevin]很快发现，当电话挂机时，它会给出一个恒定的高信号，当拿起电话时，信号会由高变低，拨打每个号码会产生一定量的高低交替的脉冲。

在本系列的第二部分中，[Kevin]真正开始解码脉冲拨号，这是第三部分音乐化时所必需的。在这里，[Kevin]添加了一个 MIDI 模块和一个 Roland MT-32 synth，将拨号盘用作 MIDI 音符发生器——拨号盘上的每个音符都会持续，直到听筒放回听筒。

第四部分集中在一个 MIDI 补丁更换。[Kevin]拿起电话，拨一个长达三位数的代码，然后挂断，这触发合成器改变到指定的声音。在第五部分，手机变成了一个随机音符序列器，同一数字的每次连续旋转都会产生一个不同的随机选择的音符。然而，这仅仅是个开始，所以我们会回来查看更新。与此同时，您可以在休息后收听音符生成器和随机音符序列器演示。

[你不想一直使用旋转式拨号盘吗](https://hackaday.com/2020/02/13/simplify-your-life-with-this-pocket-rotary-cellphone/)？好吧，只要不是紧急情况？

 [https://www.youtube.com/embed/zJhJbrmqhs0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zJhJbrmqhs0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

