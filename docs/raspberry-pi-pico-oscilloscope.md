# Raspberry Pi 微微示波器

> 原文：<https://hackaday.com/2021/06/26/raspberry-pi-pico-oscilloscope/>

当你深入电子世界的时候，一个好的示波器很快就是一个不可或缺的工具。然而，对于许多调试低压、低速电路的用例来说，昂贵的示波器只使用了其一小部分功能。作为这些用例的极简替代方案[，【fhdm-dev】创建了 Scoppy](https://github.com/fhdm-dev/scoppy) ，一个用于 [Raspberry Pi Pico](https://hackaday.com/2021/01/20/raspberry-pi-enters-microcontroller-game-with-4-pico/) 和 [Android 应用](https://play.google.com/store/apps/details?id=xyz.fhdm.scoppy)的固件组合，以创建一个功能示波器。

正如您所料，规格相当有限，在两个通道共享 500 kS/s 的速度时，最多只能捕捉 100 kpts。在没有一些额外的前端电路来保护 Pico 的情况下，输入电压被限制在 0-3.3 V，应用程序和固件都不是开源的，访问第二个通道并删除广告需要大约 3 美元的应用内购买。即便如此，我们仍然可以想到一台 7 美元左右的示波器的许多实际用途。如果您决定添加一些前端电路来改变电压范围，您可以在应用程序中设置它们，并通过拉高或拉低某些 GPIO 引脚在它们之间切换。该应用程序具有大多数基本的示波器功能，连续和单次捕捉，可调触发设置和可缩放的波形显示。

像这样简单、便宜的示波器有它们的位置，但是当你看到开发一个高性能示波器需要什么时，你就会开始理解为什么“真正的”示波器如此昂贵。