# printere 一眨眼就能给你统计数据

> 原文：<https://hackaday.com/2019/10/03/printeye-gives-you-stats-in-a-blink/>

从前，大多数东西都是单一用途的，比如怀表。然后有人做了一个有日期功能的手表，接下来你知道，我们有了电视/录像机组合和瑞士军刀。现在，人们从口袋里掏出电脑，只是为了查看时间或床上的温度。

[欧文]对这种多功能疯狂的解药是 [PrintEye，一个简单的界面，查询他的打印机，并在一对有机发光二极管窥视镜上显示其生命体征](https://hackaday.io/project/167589-printeye)。这是零件箱特价，你知道我们有多喜欢。PrintEye 通过 UART 连接到 Duet 控制器，其固件与 ATMega328P 窃窃私语。Mega 发送一个 M 命令，并以 JSON 格式返回所有状态和温度数据。然后它解析信息并在双有机发光二极管屏幕上显示出来。

想做一个吗？[Owen]在 IO 上有你需要的所有文件，但不提供手把手的服务。如果你以前从未转过板，这可能是你的入门。必须有互联网连接？查看激发 PrintEye 灵感的 Octoprint 显示器[。](https://hackaday.com/2018/11/05/esp8266-monitor-keeps-an-eye-on-octoprint/)