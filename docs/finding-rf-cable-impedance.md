# 查找射频电缆阻抗

> 原文：<https://hackaday.com/2020/05/24/finding-rf-cable-impedance/>

在 DC 和低频时，我们可以假设导线是完美的导体。不过，在无线电频率下，你需要考虑电线和电缆的许多影响。其中之一是特征阻抗。如果你有一根有标记的电缆，你当然可以在网上查找。但是如果你不知道这是哪种电线呢？在[偏移电压]的帮助下，[你可以测量它](https://www.youtube.com/watch?v=afDSE_ejTNk)，如下图所示。

这是过去需要 LCR 电桥等外来测试设备才能做到的事情之一，但如今测量电感和电容的仪表已经很常见了。诀窍很简单:测量电容，然后短接电缆的一端，测量电感。

一旦你有了这些数字，很容易做一点数学和确定阻抗。电缆有多长并不重要。长度会改变单个读数，但两个读数的比值将保持相对恒定。

如果你没有办法测量电感和电容，你总是可以[建立自己的测量齿轮](https://hackaday.com/2019/07/20/create-a-low-cost-high-accuracy-lcr-meter-with-an-stm32-mcu/)。如果你想采取不同的方法，[泰克公司向我们展示了如何在 20 世纪 60 年代用快速脉冲做到这一点。但为此，你需要一个瞄准镜。](https://hackaday.com/2016/02/21/retrotechtacular-transmission-lines/)

 [https://www.youtube.com/embed/afDSE_ejTNk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/afDSE_ejTNk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

