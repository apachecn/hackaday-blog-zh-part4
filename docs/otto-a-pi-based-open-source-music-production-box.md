# OTTO:一个基于 Pi 的开源音乐制作盒

> 原文：<https://hackaday.com/2018/08/10/otto-a-pi-based-open-source-music-production-box/>

想要一个不会破产的开源便携式 synth 工作站吗？[看看奥托](https://github.com/topisani/OTTO)。[托皮萨尼]开始奥托是著名的[少年工程 OP-1](https://hackaday.com/2017/09/05/teenage-engineering-the-raspberry-pi/) 的克隆人。然而，很快[Topisani]决定不再简单地克隆 OP-1——相反，他们在外形方面从它那里获得了很多灵感，但用户界面最终会非常不同。

硬件方面，OTTO 的核心是树莓派 3。最重要的音频接口是 Fe-Pi Audio Z V2，但也可以使用 USB 接口。48 个开关和四个旋转编码器由一对 Arduino pro 微型计算机控制，它们将数据传递给 Pi。数据通过一个 320×200 的 LCD 与用户联系起来。

软件是用 C++17 从头开始写的。如果你不是一个铁杆 C++开发者，不要担心。synth 引擎、音频效果和其他 DSP 软件是用 [Faust](http://faust.grame.fr/) 编写的，这更容易学一点。

OTTO 正在积极开发中，synth 引擎已经在运行，原型正在开发中，并且充实了 UI 编程的指南。如果你喜欢创作音乐，这个值得一试，[和 Zynthian](https://hackaday.com/2018/06/08/a-fully-open-source-raspberry-pi-synthesizer/) ，另一个基于 Raspberry Pi 的合成器。