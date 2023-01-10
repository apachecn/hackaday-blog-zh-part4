# Pi 的超级 UPS

> 原文：<https://hackaday.com/2020/11/05/a-super-ups-for-the-pi/>

在生产环境中使用 Raspberry Pi 或大多数其他系统的一个问题是处理由于断电引起的突然关机。现代操作系统通常将本应在磁盘上的数据保存在内存中，突然的电源循环会产生问题。一个答案是不间断电源，但维护电池并不好玩。[斯科特]想要做得更好，所以他用超级电容器建造了一个[UPS。](https://www.smbaker.com/supercapacitor-uninterruptable-power-supply-ups-for-raspberry-pi)

超级电容器 UPS 几乎是理想的。这种电池充电很快，不会像电池那样磨损。电容器也不在乎它们是否长时间储存。唯一真正的缺点是它们没有电池的容量，但对于像 Pi Zero 这样的小型计算机来说，很容易组合足够的电容器来完成这项工作。

特别是，[Scott 的]设计使用五个 10F 电容，每个电容充电至 2.5V。缺点是这需要 12V 电源，所以他做了第二个设计，仅使用两个电容，每个电容占用 5V 电源的一半。

将电容电压转换为所需输出电压有多种选择。还有[软件](https://github.com/sbelectronics/ups)来运行板载微控制器，并在主电源下降时强制关闭 Pi。

自然，这不是一个原创的想法，但是做得很好。你也可以购买便宜的现成的 Pi 形式的 UPS 板，但如果你使用的话，你可能想为他们检查一些[售后软件](https://hackaday.com/2019/08/27/fixing-a-cheap-ups-hat-for-your-raspberry-pi-with-a-tiny-daemon/)。

 [https://www.youtube.com/embed/j5Bv8r3TVPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j5Bv8r3TVPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

