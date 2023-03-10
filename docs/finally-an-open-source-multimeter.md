# 最后，一个开源万用表

> 原文：<https://hackaday.com/2019/06/20/finally-an-open-source-multimeter/>

为了他的 Hackaday 奖参赛作品，[【Martin】正在建造一个开源万用表](https://hackaday.io/project/165857-stm32-open-source-multimeter)，可以测量电压、电流和功率。这是一个惊人的建设，你也可以建立一个自己的。

该万用表的功能包括电压模式，范围为+/-6V 和+/-60V。有一种电流模式，基本上与电压相同，范围为+/-60 毫安和+/-500 毫安。与我们的亮黄色 Fluke 不同，它还有一个功率模式，可以同时测量电压和电流，有四种可用的范围组合。有一种连续性测试，当电阻低于 50ω时会发出蜂鸣声，还有一种元件测试模式，可测量电阻、电容和二极管。有一个完全隔离的 USB 接口，能够接收命令和传输数据，一个实时时钟，未来可能还有频率测量。

这个构建基于 STM32F103 微控制器，使用一个旧的诺基亚电话屏幕，与许多其他万用表不同，这个东西很小。它非常小。不像其他几乎所有的万用表，它小到可以放在口袋里，不用担心它。关于万用表有一件事，那就是最好的万用表是当你需要它的时候就在你手中的那一个，这个当然符合要求。

整个项目正在[写在 hackaday . io](https://hackaday.io/project/165857-stm32-open-source-multimeter)，[上，有一个针对所有硬件和软件的 GitHub repo](https://github.com/MartinD-CZ/STM32F1-open-source-multimeter)，还有一个涵盖所有功能的视频演示(如下所示)。这是一个突出的项目，也是我们迫切想得到的东西。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip) 

 [https://www.youtube.com/embed/ohOqSMUoqBM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ohOqSMUoqBM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

