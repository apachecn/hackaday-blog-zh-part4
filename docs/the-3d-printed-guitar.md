# 3D 打印吉他

> 原文：<https://hackaday.com/2018/10/10/the-3d-printed-guitar/>

我们刚刚在 Hackaday 奖中完成了乐器挑战，这意味着我们正在整理大量有创意的电子乐器。不管什么原因，我们似乎找不到许多非电子仪器。是的，MPC 很酷，但是弦和振动的空气柱也很酷。这就是这件作品的特别之处:它是一把 3D 打印的实体吉他。但它也有一个六音拾音器，指板上有灯，它可以和电脑进行纯粹的数据处理。

首先，这把吉他的构造。它大部分是 3D 打印的，身体的“框架”是由 Creality 3D 打印机制造的。这是一个栓接式琴颈，带有一个电视转播器主体，但这种吉他的核心——拾音器和琴马连接的地方——是由铝挤压制成的。另一片铝挤压材料延伸到颈部，包裹在 3D 打印的“背部”中，看起来“足够舒适”。床头是用螺栓固定在琴颈末端的，它似乎可以承受一百磅左右的拉力。该桥也是 3D 打印的，鞍座集成到打印中。传统观点认为这听起来很可怕，但是尼龙鞍座在过去是一件很过时的东西，所以我们只是想随大流。

电子设备是这个项目真正的亮点。拾音器是一个打捞罗兰 GK3 六音交易，每根弦有六个输出。这被发送到一个 Teensy 中，每个单独的字符串都有一个音频路径。音频处理发生在吉他中，延迟不到 5 毫秒，这足够快，不会成为一个可怕的干扰。

除了合成器、鼓机和电脑，过去五十年左右的技术进步并没有真正进入乐器领域。尤其是吉他手是技术恐惧者，他们讨厌 1963 年后发明的一切。虽然[Frank]的 ElektroCaster 的颈部可能感觉不太好，但这是一个非常有趣的工具，也是 Hackaday 奖的一个很好的参赛作品。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)