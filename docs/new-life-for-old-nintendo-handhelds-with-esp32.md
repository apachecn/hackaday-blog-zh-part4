# 旧任天堂掌机 ESP32 的新生活

> 原文：<https://hackaday.com/2019/08/14/new-life-for-old-nintendo-handhelds-with-esp32/>

Game Boy Pocket 是任天堂 1996 年对 1989 年经典掌机的重新设计，它的外形更小，屏幕更好，功耗更低。虽然它没有像它的前身那样成为标志性的，但它仍然有足够的受欢迎程度，让像[Eugene]这样的修改者为它创造新的硬件。他的复古 ESP32 板[是游戏机主板和屏幕](https://hackaday.io/project/166144-retro-esp32)的替代物，赋予了它全新的生命。

[![](img/a1007c7545275cbd41dfb20a706c9b7e.png)](https://hackaday.com/wp-content/uploads/2019/08/retroesp32-thumb.jpg) 【尤金】对制作这种 mod 并不陌生，他之前的 [Gaboze Pocaio](https://github.com/32teeth/GabozePocaio-Round2) 项目就用这种外形做了完全相同的事情，只是用了树莓 Pi 而不是这里使用的 ESP32-WROVER。他选择的集成 SoC 基于 ODROID-GO，这是一款类似的便携式控制台，但有自己的定制外壳。

这个项目并没有停留在硬件上，Retro ESP32(以前称为 Gaboze Express)还提供了一个用户友好的界面来启动模拟器。这个 GUI 代码也可以与 ODROID 一起使用，因为它们共享相同的硬件平台，所以如果你有其中的一个，你现在就可以从他们库的软件分支[中试用它。](https://github.com/retro-esp32/RetroESP32/tree/Software)

如果你对用更现代的硬件替换复古的技术内部部件的想法感兴趣，看看他们对这个谦逊的奥斯本 1 号或 T2 不知情的 TRS-80 100 型 T3 做了什么。可怜的家伙根本没想到会这样。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)