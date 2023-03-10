# 与 LoRa 的远程文本通信

> 原文：<https://hackaday.com/2022/05/25/long-distance-text-communication-with-lora/>

在过去二十年左右的时间里，价格合理、性能可靠的手机彻底改变了我们的沟通方式，而智能手机的采用更是加速了这种改变。如果你住在一个有蜂窝基础设施的地方，这一切都很好，但如果你住在更偏远的地区，你就必须更有创造性。例如，这种基于文本的通信设备，可以让你发送文本信息，而无需那些繁琐的基础设施。

[![](img/09cbfec06416eb0bae0937dc7ec4c1d5.png)](https://hackaday.com/wp-content/uploads/2022/05/loraqwerty_detail.jpg) 虽然【亚瑟】没有专门为离网使用创建这个项目，但它仍然是一个有趣的项目。这些设备使用物理 QWERTY 键盘和小屏幕，让人想起 2000 年代后期的黑莓设备(部分原因是他们实际上使用的是黑莓键盘)。该项目的另一个目标是低功耗，在轮询键盘、内存 LCD 以及使用 LoRa 接收和发送消息之间，[Arthur]能够将电流降至 12 mA。

在相对常见的 nRF52840 和 SX1262 芯片之间，加上[Arthur]提供原理图的事实，这对于喜欢开车到野外或住在远离城镇的地方担心手机接收问题的人来说，是一个优秀的离网设备。

在即将到来的野营旅行之前，您是否在寻找更容易组装的物品？[这款来自【MSG】](https://hackaday.com/2021/02/05/lora-messenger-does-its-best-blackberry-impression/)的类似风格的 LoRa 通信器使用现成的模块，大大减少了部件数量。离网通信的另一个选择是[使用现有的智能手机与 LoRa 网络配对，就像我们在这个项目](https://hackaday.com/2022/02/21/an-off-grid-makeshift-cell-network/)中看到的那样。