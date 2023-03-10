# 这根 3.5 毫米的电缆会扭曲信号，隐藏音频过滤电路

> 原文：<https://hackaday.com/2022/04/10/this-3-5mm-cable-distorts-signals-hides-audio-filtering-circuit/>

[Avian]的爸爸得到了一个新的带 3.5 毫米插孔的火腿无线电收发器，他的一堆电缆给他从 Bose headphones 得到了一根耳机线。他用它制作了一个 DB9 到 3.5 毫米的适配器，但它无法让数据通过，而是输出失真的波形垃圾。通过一个函数发生器和一个示波器，[Avian]绘制出了电缆的频率响应，结果发现它与直线相差甚远。发生了什么事？

拆开连接器是一件棘手的工作。钝器力和洗甲水浸泡的组合并没有完全弄好它们，所以[Avian]继续施加钝器力，以最小的伤亡将千斤顶拆开。事实证明，3.5 毫米插头确实有更多的功能——一整块 PCB 加上几个电阻和电容，逆向工程成上面看到的原理图。

看起来 Bose 决定调整一副特定耳机的音频特性，插入式滤波器不知何故是最有效的解决方案。我们可能不应该经常看到这种情况，但请记住:下次您重新使用的 3.5 毫米电缆不按预期运行时，明智的做法是使用您可信赖的电表或示波器进行电容测试。

有了[多小的 MCU 就有了](https://hackaday.com/2022/03/01/new-part-day-smallest-arm-mcu-uproots-competition-needs-research/)，你可以轻松地隐藏多个电容！我们不经常看到电缆内置电路，但当我们看到时，这是出于恶意目的的。