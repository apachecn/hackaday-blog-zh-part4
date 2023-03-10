# DIY 树莓派多外汇踏脚转盘

> 原文：<https://hackaday.com/2019/06/17/diy-raspberry-pi-multi-fx-stomp-box/>

从构建自己的模拟效果踏板到通过微控制器处理音频，许多音乐家喜欢构建自己的声音修改盒。在他的 2019 年 Hackaday 奖参赛作品中，[Craig Hissett]有一个项目是建造一个一体化多效果踏脚盒。

盒子中央是一个树莓派，配有 AudioInjector 立体声声卡。该卡负责立体声输入和输出，并将信号传递给 Pi。该软件是 Modep，一个开源音频处理器，允许设置一系列数字效果插件在 Pi 上运行。在找到一些脚踏开关后，[Craig]将它们连接到 Arduino Pro Micro，他将它设置为 MIDI 设备，向 Pi 上运行的 Modep 软件发送 MIDI 消息。

还有几个步骤要走，但是[克雷格]已经完成了基本的布局。接下来是连接它并为它构建一个合适的案例，以及处理延迟问题。几年前，另一个[多效果踏脚转盘](https://hackaday.com/2015/08/08/hackaday-prize-entry-diy-guitar-multieffects/)在 Hackaday Prize 中亮相，去年，[这款多效果控制器](https://hackaday.com/2018/10/27/hardware-controllers-for-software-effects/)亮相。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)