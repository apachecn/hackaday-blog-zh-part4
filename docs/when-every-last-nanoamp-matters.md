# 当每一毫微安都很重要的时候

> 原文：<https://hackaday.com/2018/08/18/when-every-last-nanoamp-matters/>

你可以从任何东西获得电力。你小时候制作的旧水晶收音机套件教会了你这些，但是做一些比用耳机连接散热器收听本地 AM 电台更有趣的事情怎么样？[这就是电子桶的目标](https://hackaday.io/project/159691-electron-bucket-extreme-power-management-module)。这是一种电力收集设备，可以从任何地方获取电力，无论是一片铝箔还是一束 led。

电子桶背后的基本想法是收集周围的无线电波，就像你的旧水晶无线电设备一样。有一个倍压器，一个整流器，还有一个稍微有点变化的电源管理电路，通常在电池供电的电子设备中可以找到。

当然，这种电路不仅仅可以从周围的无线电波中获取电能。通过将一束 led 连接在一起，就有可能发送几个蓝牙数据包。这非常令人印象深刻——该电路使用 led 作为太阳能电池，通常在阳光直射下以 0.5V 的电压产生约 50nA 的电流。通过并联和串联 12 个发光二极管，它设法收集足够运行一个小型无线模块的能量。这令人印象深刻，也是今年 Hackaday 奖电力采集挑战的有趣参赛作品。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)