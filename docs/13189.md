# 非接触式探头工作得更好，只是稍微复杂一点

> 原文：<https://hackaday.com/2022/03/29/non-contact-probe-works-better-with-a-little-more-complexity/>

非接触式电压探头已经出现了一段时间，现在一些测试设备已经内置了这种探头。这可能是你不太想的事情之一，但检测交流电压肯定不难。结果发现有很多电路可以做到这一点，[nsievers51]尝试了一堆。许多都不太好用，但是最好的使用了 4069 CMOS 六进制反相器。一元店的手电筒提供电源、一个盒子和一个 LED，结果是一个好看而有效的探针。

该电路来自[电子图书馆](https://www.electronicslibrary.org/)网站，对于这种设备来说相当复杂。CMOS 反相器具有高输入阻抗，因此可以拾取微弱的信号。两个反相器形成一个环形振荡器，产生 1 kHz 左右的脉冲，而不是直接驱动 LED。在该频率下，LED 看起来是亮的，但是电池消耗不太严重。单个 2N2222 型晶体管驱动 LED。

过去，我们已经看到了这个工具的许多变体。其中很多[只用晶体管](https://hackaday.com/2011/09/20/dino-builds-a-simple-non-contact-voltage-detector/)。

 [https://www.youtube.com/embed/EKpkbZPvV50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EKpkbZPvV50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

