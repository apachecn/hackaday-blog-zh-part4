# 树莓皮片获得无线电手术增强

> 原文：<https://hackaday.com/2021/10/20/raspberry-pi-tablet-gets-radio-surgical-enhancement/>

当我们购买新的平板电脑时，我们总是很兴奋。但几个月后，它通常会被压在书柜上一堆文件的底部，成为不如我们的台式电脑强大、不如我们的手机方便的受害者。然而，如果你不介意厚平板电脑，你可以让 RasPad 外壳适合你自己的树莓派，所以它可以用作平板电脑。老实说，我们并没有印象深刻，直到我们看到[RTL-SDR] [在外壳](https://www.rtl-sdr.com/raspad-3-0-review-building-a-portable-raspberry-pi-4-tablet-with-built-in-rtl-sdr/)内添加了一个 SDR 加密狗，使其成为一个非常便携的 Raspberry Pi SDR 平台。

这个盒子本身有点意思，尽管要注意它的价格超过 200 美元。以这个价格，你可以得到一个 LCD 和驱动板，一个电池系统，扬声器和一个 SD 扩展槽，上面有一些音量和亮度的控制按钮。下面是整个场景的视频(德语)。

整个东西重约 1 公斤，对于平板来说有点重。它也相当厚，尽管这有利于进行这种修改，并且当它平放在桌子上时，也给了触摸屏一个很好的角度。

大多数 Raspberry Pi 软件都不是为触摸屏设置的，但这篇文章解释了他们在使用不同的 Linux 版本而不是外壳制造商的默认平板软件时发现的一些问题。

我们担心外壳内的 SDR 会受到干扰，但显然，有了外部天线，干扰可以忽略不计。但是，当使用通过附加的 RF 连接器直接连接到盒子上的天线时，您可以看到干扰。如果您使用没有适当屏蔽的 SDR 加密狗，结果可能会更糟。

我们认为我们可能更喜欢更具未来感的外形。你也可以获得直接与树莓 Pi 一起工作的[SDR。](https://hackaday.com/2021/06/20/raspberry-pi-hat-adds-sdr-with-high-speed-memory-access/)

 [https://www.youtube.com/embed/AzzueFF1JYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AzzueFF1JYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

