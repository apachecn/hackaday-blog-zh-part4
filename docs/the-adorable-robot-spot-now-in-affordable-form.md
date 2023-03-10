# 可爱的机器人斑点，现在价格适中

> 原文：<https://hackaday.com/2020/10/23/the-adorable-robot-spot-now-in-affordable-form/>

如果你一直在关注波士顿动力项目 Spot，你会看到它的功能，以及自去年正式发布以来，我们如何开始看到它在公共场合被更多地使用。但是，在过去几年里，业余爱好者电子产品如何发展并赶上大公司的真实展示中，[Miguel Ayuso Parrilla]向我们展示了他自己对带[CHOP 的步行机器人的看法，他是今年 Hackaday 奖](https://hackaday.io/project/171456-diy-hobby-servos-quadruped-robot)的决赛选手之一。

CHOP 是一个 DIY 四足机器人，它的工作方式与 Spot 非常相似，尽管它的外形更小，而且最令人印象深刻的是，它的材料清单可以在 500 美元以下获得。整个项目是开源的，这意味着任何人都可以用现成的部件和一些 3D 打印来构建自己的版本。然而，如果你不能得到硬件，[你仍然可以玩在调试过程中使用的 PyBullet 模拟机制](https://hackaday.io/project/171456-diy-hobby-servos-quadruped-robot/log/183647-pybullet-simulation-example)。

主持这场演出的是两个主要组件，一个是 Raspberry Pi 4B，一个是 Arduino Mega。Mega 与伺服控制器接口，并为惯性测量单元等传感器提供过滤，Pi 接收所有数据，并使用一系列 Python 脚本来确定机器人的步态，以及伺服系统应该通过反向运动学模型以何种方式移动。为了控制机器人身体加速的方向，蓝牙遥控器向 Raspberry Pi 发送命令。

我们很高兴看到本土项目上升到这种复杂程度，这在几年前的创客界几乎是闻所未闻的，只有拥有大量研发资金的大型科技公司才会出现。除了 Spot，还有其他四足机器人可以激发你的灵感，比如这个球形设计和折叠腿的机器人。休息之后看看这个。

 [https://www.youtube.com/embed/TBHhbgf6zaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TBHhbgf6zaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/n7NX-Sw5sl4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n7NX-Sw5sl4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)