# 基于概率的鼓手让节拍听天由命

> 原文：<https://hackaday.com/2019/07/23/probability-based-drummer-leaves-the-beats-up-to-chance/>

鼓机可能看起来像是硬件制造商的许多仪式之一，它们是一个概念，你可以简单地实现它，或者把它变得非常复杂。[【马特的】DrumKid 就是其中的一个](https://hackaday.io/project/164521-drumkid-aleatoric-drum-machine)，它漫长的发展历史在项目日志中有精彩的记载。

[Matt]的初衷是将自动鼓手作为乐队的一部分，希望“拥有优秀鼓手的表现力，但没有简单鼓机的机器人倾向”。为此，他创建了 DrumKid 的第一个版本[，这是一个使用网络音频 API](https://hackaday.io/project/164521/log/162373-drumkid-a-history) 的基于网络的项目。界面由显示不同设置水平的条组成，可以直观地调整，改变鼓声音播放的概率。这给了“鼓手”它的不可预测性，将它自己与任何常规的老式鼓机区分开来。

几年后，[Matt]现在想把他的 DrumKid 改造成一个合适的音乐设备，把这个概念移植到一个独立的硬件鼓机上，你可以把它插到你的混音器上。他决定为他的项目使用 Arduino 框架，而不是 Teensy 平台，以便降低构建成本。控制被简化为几个按钮和电位计，整个系统由三节 AAA 电池供电。此外，像这样针对硬件的项目允许添加新的功能，如位粉碎过滤器。

我们已经在 Hackaday [上看到了第一个原型，当时它出现在 Hackaday 奖导师会议](https://hackaday.com/2019/06/28/mitch-altman-mentors-manufacturing-with-hackaday-prize-expert-session/)上，很高兴看到该项目自那以后如何发展。经过多次修改，新的原型从青少年工程公司的“口袋操作员”鼓机中获得了设计线索，使用主 PCB 作为自己的面板，而不是 3D 打印的外壳[，这是我们以前见过的熟悉方式](https://hackaday.com/2019/01/22/a-drum-set-in-your-pocket/)。不幸的是，由于布线错误，最新的电路板无法工作，但你可以在他的项目日志中看到以前的工作原型。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)