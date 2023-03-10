# 鱼鹰键盘让 NRF52840 展开翅膀

> 原文：<https://hackaday.com/2022/12/08/osprey-keyboard-lets-the-nrf52840-spread-its-wings/>

虽然大多数人不在乎用一个手指还是十个手指，但有些人想通过学习如何触摸打字来提高自己。老实说，没有比进入 ergo 键盘游戏更简单的方法了。即使你认为自己已经是一个触摸式打字员，直排式或列交错式键盘可能会教你其他方式，因为你会发现自己试图用食指键入“c ”(例如),结果惨败。

[![](img/585fa47e8baa2d4632cdcd6da10e22ca.png)](https://hackaday.com/wp-content/uploads/2022/12/osprey-inner.jpg) 【艾巴斯特勒】选择了所有路线中最好的一条[决定建造自己的完美键盘，叫做鱼鹰](https://mpwr.xyz/projects/osprey.html)。这是一个无线的，列交错 40%运行在 ZMK 固件，这当然是开源的，因为是 PCB 本身和厚和旅行准备印刷外壳。虽然[ebastler]还没有实现这些附加输入中的任何一个，但 Osprey 也支持拇指棒和跟踪板。

就大脑而言，它是一个裸露的 nRF52840 芯片和一个 TI BQ24075 用于电池充电。关于这个实现有趣的事情是[ebastler]使用并滥用了 [Nordic sample schematic #4](https://infocenter.nordicsemi.com/index.jsp?topic=%2Fps_nrf52840%2Fref_circuitry.html&cp=4_0_0_6_2_3&anchor=unique_609532902) ，它利用了芯片的两个 DC-DC 转换器级。我们迫不及待地想看看这个开创性的构建对社区意味着什么！