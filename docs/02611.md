# ATtiny 项目的主电源可能是个坏主意

> 原文：<https://hackaday.com/2019/04/02/mains-power-supply-for-attiny-project-is-probably-a-bad-idea/>

为小负载 DC 电路设计市电电源时，需要考虑很多因素。小尺寸、高效率和材料成本都跃入脑海。潜在的杀伤力似乎是一件坏事，但这并没有阻止[伟大的斯科特！]来自[探索容性压降电源](https://www.youtube.com/watch?v=-n22cqZkxNQ)。你知道，为了科学。

这里的背景故事是[伟大的斯科特！]正在进行一项需要断电的绝密 ATtiny 项目。对于此类应用，开关电源实际上是必要的，但与预期的微控制器电路相比，它们实际上相当大，而且以前也是如此。所以为了学个一二，【斯科特！]设计了一个电容性降压电源，电容的电抗就像一个降压电阻一样限制电流。他的第一次尝试只是一个电容器和一个 LED 串联；这对 LED 来说并没有什么好结果。

为了了解原因，他对一些低电流电源设备进行了逆向工程，发现实用的电容降压器需要更多的元件，主要是一个串联电阻以防止涌入电流失控，但也需要一个桥式整流器和一个齐纳二极管来箝位。将所有这些连接起来会产生一个工作的电容性降压器电源，但其成本与一个小型开关一样大，而且如果电源插错了，还有可能致命。边注:我们以为德国线电线极化，以防止这一点，但显然不是？(编者注:[没有](https://en.wikipedia.org/wiki/AC_power_plugs_and_sockets#CEE_7/3_socket_and_CEE_7/4_plug_(German_%22Schuko%22;_Type_F))！)

一如既往，甚至当【伟大的斯科特！]的项目并不完全成功，就像[一个次优的 3D 打印 BLDC](https://hackaday.com/2018/12/18/can-you-3d-print-a-stator-for-a-brushless-dc-motor/) 或[为什么不麻烦去建造你自己的 DC 交流逆变器](https://hackaday.com/2018/09/30/how-to-build-an-inverter-and-why-not-to-bother/)，我们享受由此产生的学习。

 [https://www.youtube.com/embed/-n22cqZkxNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-n22cqZkxNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

