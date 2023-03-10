# 3D 打印机卫士观察最坏情况下的故障

> 原文：<https://hackaday.com/2018/07/16/3d-printer-guardian-watches-for-worst-case-failures/>

有些设备只有一项工作要做，但这项工作可以有许多方面。对[jmcservv]来说，这方面的一个例子是在 3D 打印机中防止最坏情况故障的工作，这促使他开发了 [3D 打印机看门狗守护者](https://hackaday.io/project/159238)。当谈到火灾时，二级保护是游戏的名称，因为检测热失控和关闭加热器是一回事，但如果这还不够呢？控制加热器的 MOSFET 可能关闭失败，无法再正常关闭。在这种情况下，需要某种备份。当然，保护系统也应该通知操作者任何严重的问题，但是最好的方法是什么呢？这些都是[jmcservv]正在努力解决的问题，他的看门狗不仅会密切关注系统中的任何发热元件，还会因此采取各种行动。

有些结果(如火灾)已经足够糟糕，值得额外的工作和额外保护的成本，这就是促使[jmcservv]提交其看门狗系统以获得 Hackaday 奖的想法。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)