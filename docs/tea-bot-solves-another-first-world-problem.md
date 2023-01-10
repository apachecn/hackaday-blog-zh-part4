# 茶机器人解决了另一个第一世界的问题

> 原文：<https://hackaday.com/2019/07/24/tea-bot-solves-another-first-world-problem/>

在电影《瓦力》中，未来的人类住在漂浮的椅子上，一切都为他们做好了。今天，如果我们不得不亲自去找电灯开关或遥控器，我们会发牢骚。带屏幕的漂浮椅能有多远？茶机器人 T2 让我们离那个目标更近了一步。使用激光切割框架，ESP8266 和伺服电机，T2 沏茶的时间正好合适。

我们有点希望机器人至少能泡进和泡出茶叶袋，但它确实提供了一个让你选择冲泡方式的网络界面。当然，[代码是可用的](https://github.com/rachel-lynch-lin/esp8266_tb_web_server)，所以你可以进行修改——也许打开杯子下面的电热板。

虽然这对大多数人来说不是特别实用，但这是一个很好的简短示例，说明了如何提供 web 界面并使用 ESP8266 做一些事情。也许你想锁一个抽屉或者把一个棉花糖放入火焰中，对于这些任务，你可以使用非常相似的代码。

由于伺服系统采用脉冲宽度，消耗的电流很少，如果你在为一群人服务，你可以驱动一堆伺服系统，并行处理很多茶杯。自然，这不是我们见过的第一个自动化的啤酒酿造商。它甚至不是唯一一个有[伺服](https://hackaday.com/2015/09/13/brewing-tea-too-stressful-3d-print-a-tea-steeper/)的。

 [https://www.youtube.com/embed/yVVh1pdxSX0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yVVh1pdxSX0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

