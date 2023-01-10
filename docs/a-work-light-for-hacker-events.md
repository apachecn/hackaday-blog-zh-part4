# 黑客事件的工作灯

> 原文：<https://hackaday.com/2019/05/31/a-work-light-for-hacker-events/>

如果你曾经参加过黑客训练营，你就会知道这样一个问题:一个帐篷区只有透过薄雾的激光照明，远处传来电子舞曲的重击声。你需要 T1 来完成这个项目，但是太阳已经下山了，你的包里没有空间带探照灯。

在过去的日子里，你可能会在一个空的俱乐部队友瓶子里插上一支闪烁的蜡烛，然后继续前进，但这是 21 世纪。[【Jana Marie】为您提供了解决方案](https://hackaday.io/project/165137-enlightened-otter)，她的俱乐部队友瓶不是蜡烛，而是放在一堆 LED 装饰的印刷电路板上面，锂离子电池提供高强度筒灯。这不仅仅是一个简单的灯，它通过顶部表面的触摸控制来实现可变的亮度和色温，以及为额外的 18650 个电池充电的能力。它的核心是一个 STM32F334 微控制器，巧妙利用其板载定时器来驱动升压转换器，电源输入通过 USB-C。

我们第一次看到这个项目的早期成果是在去年的 [EMF 2018 黑客营](https://hackaday.com/2018/10/05/electromagnetic-field-2018-event-review/)上为一个黑暗的 Hacky Racer fettling 提供照明，自那以来它已经做了一些修改。[这都是开源的](https://github.com/Jana-Marie/Enlightened-Otter)，所以如果你喜欢，你可以自己尝试一下。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)