# 租赁房屋恒温器无需修改哑控制器即可实现智能升级

> 原文：<https://hackaday.com/2020/02/09/rental-home-thermostat-gets-smart-upgrade-without-modifying-the-dumb-controller/>

住在出租房里的人面临的一个问题有两个方面:这种房子很少有供暖控制器等最新设施，房东往往不喜欢房客自己安装替代设备。[Andy]想要升级他家的加热控制器，并且处于这种情况下，所以[他为现有的机械计时器](https://andybradford.dev/2020/02/01/how-i-made-my-heating-smart-without-damaging-or-replacing-anything/)设计了一个智能控制器附件，它不会不可逆转地修改任何东西，并且在他移动时可以轻松移除。

这听起来像是一个不可能的任务，但他通过在定时器开关上方的 3D 打印框架上安装步进电机，完成了这项任务。这是一种带有电动环的类型，塑料手指可以放在环上来打开或关闭开关；他只是简单地移除了塑料手指，并为电机设计了一个轴延伸，模拟它们通过开关。他现在可以从一个 ESP8266 上随意打开和关闭暖气，在这种情况下是在一个 Adafruit Feather Huzzah 上。

这一切的背后是一个定制仪表板的 Adafruit IO，如果你想了解它的功能，Hackaday 的肖恩·博伊斯(Sean Boyce)[试用了这项服务。对于这个项目，Adafruit IO 交付了[Andy]想要的东西，但仍然留下了一些初期问题。需要告诉步进器不要试图保持其位置，并且非常缓慢地移动步进器会产生足够长的等待时间来触发 ESP 的看门狗定时器。加上](https://hackaday.com/2017/10/31/review-iot-data-logging-services-with-mqtt/) [IFTTT](https://ifttt.com/) 让他有能力安排时间，以及 Alexa 控制。总而言之，他以更低的成本复制了一些商业产品，而且没有惹恼他的房东。你可以在休息时间下面的视频中看到它的运行。

 [https://www.youtube.com/embed/DLs6QLKgmIc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DLs6QLKgmIc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

