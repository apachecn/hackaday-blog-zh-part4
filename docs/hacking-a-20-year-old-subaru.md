# 黑了一辆 20 年的斯巴鲁

> 原文：<https://hackaday.com/2018/12/31/hacking-a-20-year-old-subaru/>

虽然汽车正慢慢变得完全由计算机控制，但自 20 世纪 70 年代以来，公路车辆一直依赖于计算机。计算机的第一次汽车应用是在发动机控制单元(ECU)中，这是随着燃油喷射系统开始取代化油器而出现的。

[P1kachu]的 1997 款斯巴鲁翼豹 STi 与该年份的大多数汽车一样，使用 ECU，并为外部通信提供诊断连接器。【P1kachu】的[斯巴鲁黑客项目](https://p1kachu.pluggi.fr/project/automotive/2018/12/28/subaru-ssm1/)包括构建诊断接口设备，转储 ECU 的固件，逆向工程二进制理解并禁用限速器。如果这看起来很熟悉，那是因为[我们刚刚在周六](http://hackaday.com/?p=338371)讨论了这辆车的信息娱乐黑客。但他补充说，关于通信协议的信息绝对值得再看一看。

这个时代的斯巴鲁使用了一种称为 SSM1 的非标准诊断协议，它本质上是一种 5 伏 TTL 串行线，以每秒 1953 位的速度运行。自定义接口由一个 Teensy 和一个 3.3V 至 5V 电平转换器组成。一旦连接，命令可以直接发送到 ECU。幸运的是，该协议在过去已经被很好地记录了。通过反复发出“从 ECU 地址读取数据”命令，可以转储完整的固件。

[P1kachu]继续查找各种发动机调谐图，并探索限速器的内部工作原理。随着汽车越来越电脑化，很高兴看到人们仍然能够调整他们的乘坐，即使这意味着使用 Teensys 而不是扳手。