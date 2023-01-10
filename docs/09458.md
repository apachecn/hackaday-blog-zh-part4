# IEEE 制造了一款智能手表

> 原文：<https://hackaday.com/2021/03/06/the-ieee-builds-a-smart-watch/>

过去，制造自己的手表要么是一个大项目，要么意味着你并不真正关心你手腕上的东西是什么样子。但是现在有了现代零件和制造技术，一款好看的智能手表不再是家庭商店买不到的了。但是如果你不想完全自己做，你可以求助于一个工具包，这就是斯蒂芬·卡斯所做的。他在 IEEE Spectrum 中写道，他拿了一个叫做 Watchy 的工具包，为你测试它。

Watchy 是一款[开源产品](https://github.com/sqfmi/Watchy)，使用了一个 ESP32，一个电子墨水显示屏，[售价约 50 美元](https://www.tindie.com/products/sqfmi/watchy/)。显示屏为 1.5 英寸，对于手表来说足够好了，它有一个实时时钟，一个振动马达，一个加速度计和四个按钮。整个系统依靠 200 毫安的锂聚合物电池运行。充电器是 microUSB，你也可以使用常用的 Arduino 工具向它上传软件。

然而，[斯蒂芬]发现他尝试的例子一开始都行不通。他发现 Mac 软件有问题，但他在 Windows 下也有问题。答案？换成树莓派似乎很管用，一旦手表被擦干净，Mac 工具也能工作。听起来这不是一个常见的问题，但他必须在每个编程周期之前用圆周率擦除手表。

与普通的 Arduino 程序不同，典型的 Watchy 程序中的所有工作都发生在`setup()`中，因此手表大部分时间都可以休眠，并且通常每分钟更新一次 200×200。作为一个例子，[Stephan]写了一个使用古老的爱尔兰字母来显示时间的表盘。他计划添加代码来获取在线数据，并且该手机支持无线连接和解析 JSON，使这类任务变得更容易。

我们一直认为 [EZ430-Chronos](https://hackaday.com/2020/12/22/ti-ez430-chronos-turned-medical-alert-wearable/) 是一块好看的手表，但它的屏幕现在已经过时了。还可以捡很多便宜的进口手表[可以黑](https://hackaday.com/2020/05/02/cheap-smartwatch-hacking-to-run-your-own-code/)。