# ESP32 高科技施舍系列

> 原文：<https://hackaday.com/2019/07/17/high-tech-alms-collection-with-the-esp32/>

在一个理想的世界里，商店空间、工具和组件都是免费的。但是，在我们实现《星际迷航》的乌托邦之前，黑客空间将不得不依靠社区的捐赠来维持运营。虽然要钱，但如果你设计并建造一个联网的捐款箱，至少你可以从中得到一些乐趣[。](https://hackaday.io/project/162018-donationboxv3)

T2，或者至少这是(戈兰·马霍夫里奇)为萨格勒布的 Radiona hackerspace 所做的。他不满足于仅仅在鞋盒顶部开一个口子，他提出了一个实物捐赠系统，不仅为捐赠人提供了更多信息，也为募捐者提供了更多组织。

钥匙是 SparkFun 的街机式可编程硬币接收器。当连接到一个微控制器上时，这个盒子就可以记录下投入了多少钱。通过使用 RFM96 LoRa 模块，它甚至可以在保持移动的同时报告当前的运输情况；非常适合黑客空间在他们的大本营之外举办活动。

但是对于像 ESP32 这样功能强大的微控制器来说，计算硬币可不是一件容易的事情。所以[Goran]给芯片增加了几个按钮和一个液晶显示器，让它在空闲时间有事可做。这使得用户可以滚动浏览各种寻求捐赠的项目列表，并决定他们想要在经济上支持哪一个。当捐款箱计算投入了多少钱时，它会记录下这笔钱被指定用于哪个项目。

当然，如果你更喜欢自由市场做它的事情，我们已经看到这个硬币接收器被用来建造一个储物柜大小的自动售货机。或者如果你觉得自己很狡猾，你可以[试着用纸板做一个。](https://hackaday.com/2018/06/09/no-microcontroller-in-this-vending-machine-doh/)

 [https://www.youtube.com/embed/g7JSQfqqEvs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/g7JSQfqqEvs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

