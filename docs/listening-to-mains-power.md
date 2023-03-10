# 监听电源

> 原文：<https://hackaday.com/2018/08/23/listening-to-mains-power/>

通过查看主电源的波形，可以了解很多信息。谐波、瞬态变化和周期性波动与电网本身的需求相关。频率偏移会告诉你你的时钟运行得有多快或多慢，你家附近的某个地方可能有人用绝缘很差的电力线通信。通过观察插座输出的波形，你可以学到很多东西，但你如何利用它呢？【大卫】正在用[一个 PC 声卡和一些真正有趣的硬件](https://hackaday.io/project/79848-grid-2-audio)做这件事。

Grid 2 音频模块是[David]今年 Hackaday 奖的参赛作品，它由三个主要部分组成。首先是设计的机械部分。它以 IEC 电源插座的形式出现，带有内置开关、保险丝和照明。当然，你可以简单地*购买*其中的一个，但是【David】正在自学 Autodesk Inventor，你必须从某个地方开始。该构建的第二部分是 PCB 电源和市电输入。这基本上是一对变压器、一个 PCB 和一大堆隔离，使它成为一个安全的电路板。第三部分是信号调理板，将波形发送到 3.5 毫米插孔，便于任何音频采集硬件处理。

到目前为止，该板最难的部分是 PCB 设计，为此[David]全力以赴。这个东西上有一些大而多肉的痕迹，电路板的高压和低压部分之间有真正的隔离。最终结果是将电源波形发送到声卡，便于 MATLAB 处理，以及由此带来的所有好处。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)