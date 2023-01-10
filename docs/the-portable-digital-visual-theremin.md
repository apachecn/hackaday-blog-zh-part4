# 便携式数字可视特雷门琴

> 原文：<https://hackaday.com/2018/11/01/the-portable-digital-visual-theremin/>

出于某种原因，当人们想到电子乐器时，首先想到的就是特雷门琴。也许这是因为它可以说是第一个纯粹的电子乐器，或者因为没有机械模拟的东西可以简单地通过挥动你的手来发出声音。这个项目采纳了这个想法，并将其发展到 11 个。这是一个由红外线反射器控制的便携式合成器。只要在它面前挥挥手，这就是 pitch 将要发出的声音。

这个合成器的音频硬件，就像今年 Hackaday 奖的乐器挑战中的许多获奖者一样，基于 Teensy 及其令人难以置信的音频库。该代码由两个振荡器和一个粉红噪声发生器组成。按下按钮一激活振荡器，频率由红外传感器决定。第二个按钮在各种波形中循环，而第三个和第四个按钮则上下移动八度音程。输出是 I2S，从那里一切都是一个放大器和扬声器。

当然，除非它看起来很酷，否则它真的不是一种乐器，这也是这个项目真正伟大的地方。这是一个完全 3D 打印的外壳，实际上看起来很好。有一个 8×8 LED 阵列来显示电流波形，这实际上可能是一个产品，而不是一个项目。这是一个很棒的合成器，我们很高兴让它参加 Hackaday 奖的竞选。

 [https://www.youtube.com/embed/qyO1_fC_Kus?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qyO1_fC_Kus?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/aUcpQy3lOxo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aUcpQy3lOxo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)