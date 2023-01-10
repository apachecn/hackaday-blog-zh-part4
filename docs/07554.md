# 由于 PWM 谐波，通过 RF 驱动 PAL 电视

> 原文：<https://hackaday.com/2020/08/26/driving-a-pal-tv-over-rf-thanks-to-pwm-harmonics/>

虽然大多数模拟电视在黄色 RCA 插孔上带有复合视频输入，但该功能并不通用。这个问题在 20 世纪 80 年代更加普遍，大多数家用游戏机通过用 RF 调制器将视频馈送到电视调谐器来解决这个问题。[Manzel Seet]就有这样一台使用 PAL 标准的电视机。想要显示来自微控制器的图像，他组装了 PAL-Streamer。

这个项目的目标是在模拟电视上显示图像，在[Manzel]现有的硬件上投入最少。为此，该项目使用 STM32F411 Nucleo 开发板构建。能够以高达 100 MHz 的时钟速度运行，有足够的咕噜声来处理要求苛刻的任务，如向电视输出视频信号。

为了实现 VHF 频道 3 的目标频率(61.25 MHz)，[Manzel]受到[[CNLohr]at tiny NTSC 项目的启发，选择依靠板载 PWM 硬件。](https://hackaday.com/2015/02/26/attiny85-does-over-the-air-ntsc/)该项目利用了方波的奇次谐波。将 PWM 输出设置为 6.86 MHz，九次谐波最终约为 61.71 MHz，非常接近电视机的调谐频率。完成困难的部分后，[Manzel]实现了一个虚拟的 COM 端口，允许连接的 PC 向显示器发送 PNG 图像或 GIF 动画。

这是一个有趣的项目，它表明，如果你愿意发挥创造力，就有可能驱动各种模拟显示器。对于那些渴望重新创作作品的人来说，GitHub 上有一些文件。[Manzel]指出，这种方法确实会在周围频段产生大量 RF 能量，但对于直接连接到天线输入来说，它工作得很好。我们喜欢看到微控制器上的创意视频项目，所以如果你已经知道如何让 Arduino Uno 通过 HDMI 实现 1080P，[请务必让我们知道](http://hackaday.com/submit-a-tip)。休息后的视频。

 [https://www.youtube.com/embed/O6DGFEbg23w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O6DGFEbg23w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2020](https://prize.supplyframe.com)主办单位:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)