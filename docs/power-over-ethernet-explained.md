# 以太网供电，解释

> 原文：<https://hackaday.com/2022/12/08/power-over-ethernet-explained/>

大多数读者都熟悉某种形式的以太网，特别是可能缠绕在我们长椅后面的 Cat5 电缆。同样，我们将使用以太网供电(PoE)为网络摄像头等设备供电。买一台 PoE 路由器或交换机，插上电缆，就可以上路了！但是爱伦坡背后是什么，它是如何工作的？[【Alan】根据使用技术](https://hackaday.io/project/188560-what-is-poe-my-tough-poe-development-process)的经验，撰写了一份全面的指南。

我们首先得到的是所涉及的各种地形的概要。然后[Alan]深入探讨了 PoE 端口轮询要连接的 PoE 设备、识别它并提升电压的方式。解释各种不同的电路特别有价值。展览的最后一部分是 PoE 模块的设计，使用小型开关电源提供所需的 48 伏电压。

总而言之，这应该是任何使用以太网的人的必读之作，因为它是那些经常被描述成黑匣子的东西之一。如果你想知道更多，[这是一个 Hackaday 过去也曾接触过的话题](https://hackaday.com/2019/10/24/how-power-over-ethernet-poe-works/)。