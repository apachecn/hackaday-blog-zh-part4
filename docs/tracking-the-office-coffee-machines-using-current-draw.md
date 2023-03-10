# 使用电流追踪办公室咖啡机

> 原文：<https://hackaday.com/2018/08/24/tracking-the-office-coffee-machines-using-current-draw/>

咖啡是黑客、IT 工作者以及显然也是黑客的 IT 工作者的命根子。【Omerfarukz】显然是后者。他是分布在多个楼层的大型团队的一员，所有团队都有咖啡机，任何一台都是公平的游戏。问题是知道哪一个有准备好倒的咖啡。他需要一种非侵入性的方法来监控咖啡机。

在考虑了几个解决方案后，他选择了一个不会冒犯咖啡之神的方案。这些机器使用高电流来产生热量，所以他为这些机器改装了一些旧的遥控电源插座，现在可以插入这些插座来监控电流。高电流意味着咖啡正在冲泡，他知道冲泡每杯咖啡需要一分钟，所以高电流的持续时间告诉他杯子的数量。

由于电流感应变压器没有成功，他选择了 ACS712 芯片，其核心是霍尔效应传感器，输出与测试电流成比例的电压。它到达 ATtiny 的 IO 引脚，并从那里通过串行到达 ESP8266，然后到达 Google Firebase 进行处理并通知需要刺激的 IT 工人。对于那些希望参与的人来说，[他已经在 Github](https://github.com/omerfarukz/coffee-ready) 上发布了这条赛道。

我们已经看到了其他一些非侵入式的监控方法。例如，有[用浴室秤称机器的重量](https://hackaday.com/2013/09/02/monitoring-a-coffee-pot-with-an-arduino/)和[更手动的电话通知报警按钮](https://hackaday.com/2015/07/24/alarm-notifies-the-office-when-the-coffee-is-ready/)。