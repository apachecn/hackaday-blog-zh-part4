# 一道冷光温暖你的心

> 原文：<https://hackaday.com/2022/10/09/a-cold-light-to-warm-your-heart/>

万圣节很快就要到了，还有什么比[Wagiminator]可爱的[new candle tea light](https://oshwlab.com/wagiminator/attiny85-neocandle-dip)模拟器更好的方式来增加你的万圣节装饰呢？

[Wagiminator]修改了一个 3D 打印的幽灵,并扩展了[Mark Sherman]的灯光模拟代码，以创建一个可爱的灯光，非常适合假期。NeoCandle 使用 ATtiny85 芯片为四个 WS2812 新像素果冻豆 led 供电。该设备有一个红外(IR)接收器，能够从一个讲 NEC 协议的遥控器控制它。有一个光线传感器，当它检测到环境光时，该单元可以变暗，整个单元通过微型 USB 连接断电。

ATtiny85 具有有限的程序闪存，并且[Wagiminator]在这样一个小封装中集成了许多功能，在仅 18 字节的闪存中挤进了一个位碰撞的 NeoPixel 驱动程序，该驱动程序可以推出 762 kpbs 的传输速率来更新 led。伪随机数使用 Galois 线性反馈移位寄存器，以 86 字节的闪存形式输入，其中 IR 接收器实现代码最大，使用 234 字节的闪存。ATtiny85 本身有 8 KB 的闪存，因此也许有可能将[Waginminator]的代码推到 ATtiny 系列中更具限制性的 Atmel 设备上。

随着微控制器和发光二极管变得如此便宜和普遍，用它们制作逼真的火焰变得越来越容易，正如我们在以前的电子蜡烛项目中看到的那样。

 [https://www.youtube.com/embed/n4UFV3BMcBM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n4UFV3BMcBM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

