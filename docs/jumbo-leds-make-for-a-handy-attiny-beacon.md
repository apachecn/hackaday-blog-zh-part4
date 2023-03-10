# 巨型发光二极管是一个方便的 ATtiny 灯塔

> 原文：<https://hackaday.com/2019/05/01/jumbo-leds-make-for-a-handy-attiny-beacon/>

灵感可以来自任何地方。有时候，只是看到一个有趣的部分，你非常想摆弄它，以至于你最终围绕它开发出一个完整的想法，甚至可能是产品。这就是[【Bobricius】如何发现自己创造了这个非常光滑的小警告信标](https://hackaday.io/project/164369-jumbo-led-circular-beacon)，看看最终结果，我们认为他做出了正确的决定。

[![](img/26f3d2f9bcd29db7d11e621d688d2eea.png)](https://hackaday.com/wp-content/uploads/2019/04/ledbeacon_detail.jpg)king bright DLC-6 SRD“jumbo”LED 实际上是内置在塑料扩散器中的六个独立发射器。与设备的接口足够简单；每个 LED 都有正常的阳极和阴极引脚，你只需给它们通电。[Bobricius]所创造的是一个简单的 PCB 设计，DLC-6SRD 可以直接插入其中，另一侧有一个 2032 硬币电池座。

当然，仅仅同时点亮所有六个元素不会很有趣。[Bobricius]在一些 Charlieplexing 的帮助下，通过 ATtiny10 的数字引脚单独控制它们。这使得各种有趣的模式成为可能，正如休息后的视频所示，该项目的当前迭代使用一些非常简单的代码来“旋转”LED，就好像它是紧急车辆上的闪光灯一样。

增加几个闪烁的发光二极管[可以在夜间能见度方面创造一个不同的世界](https://hackaday.com/2018/02/28/cheap-and-easy-helmet-lights-for-the-kids/)，因此一个添加如此独特光模式的廉价粘贴模块可能是一个非常重要的安全设备。随着[美国联邦航空局的新规定要求夜间飞行](https://hackaday.com/2019/02/04/faa-proposes-refined-drone-regulations/)使用防撞灯，它对无人机也很有用。

 [https://www.youtube.com/embed/m3hHpNY-EHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m3hHpNY-EHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)