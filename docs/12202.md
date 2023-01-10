# 圣诞树印刷电路板只是节日欢乐的把戏

> 原文：<https://hackaday.com/2021/12/15/christmas-tree-pcb-just-the-trick-for-festive-glee/>

节日通常是拿出工具，做一个有趣的小项目的好理由。[Simon]想要一个小装饰品在假期分发出去，所以他们很快就做了一个实际上兼容 Arduino 的圣诞树 PCB。

![](img/4fdd9ff2f5071ec36305ee630981a4b4.png)

O’ Christmas Tree, on PCB…

这是一个前瞻性的项目，包括 USB-C 连接器，在另一个连接器标准出现之前，它将在一段时间内经得起考验。当插上电源时，像许多类似的项目一样，它以喜庆的方式闪烁一些 APA102 LEDs。PCB 也加入了这个有趣的行列，白色的丝网印刷小玩意被阻焊膜上的缝隙创造出的金色小玩意增色不少。

ATTiny167 是操作的大脑，[使用与 DigiSpark Pro 开发板类似配置的微核引导加载程序](https://hackaday.com/2014/03/04/interrupt-free-v-usb/)。它依靠一个有点粗糙的低速 USB 接口进行编程，但功能对最终用户来说基本上是透明的。它可以很容易地从 Arduino IDE 中进行编程。

这无论如何都不是一个先进的项目，但它是一个可爱的赠品，可以像一张精美的 PCB 名片一样给人留下好印象。它还可以作为一个简单的工具，向新的制造商介绍可寻址 led。与此同时，如果你一直在实验室里编造你自己的假期计划，不要犹豫[给我们写信吧！](http://hackaday.com/submit-a-tip)