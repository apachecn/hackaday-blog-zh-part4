# 使用 ESP8266 磁力计检测汽车

> 原文：<https://hackaday.com/2019/09/10/detecting-cars-with-an-esp8266-magnetometer/>

在你的车道上安装一扇电动门是很棒的，但前提是要有一种简单的方法来启动它。[Andrew]说他父母家的大门只能通过手动按下面板上的按钮来控制，或者用一个没有他们想要的范围的小遥控器来控制。所以他决定[制造自己的磁力计，让大门在汽车试图离开时自动打开](https://hackaday.io/project/167542-vehicle-detection-with-d1-mini-and-magnetometer)。

自然，有商业产品可以解决这个问题。但是标价超过 150 美元，[Andrew]非常乐意花点时间修修补补，以不到 1/10 的成本完成 ESP8266 和 QMC5883X 系列磁阻传感器的工作。当然，这是那些在你脑海中看起来足够简单的项目之一，但最终需要一点技巧才能在现实世界中实现。

[![](img/838369d9d4d8fb1ed1d1e27101580601.png)](https://hackaday.com/wp-content/uploads/2019/09/espmag_detail.jpg) 举个例子，[安德鲁]必须想办法防止误报。几乎任何足够靠近传感器的物体，包括他的手，都会引起它的反应。他最终想出了一个方法，用滚动平均值来防止门仅仅因为一只松鼠跑过去就开火。内置安全装置旨在确保只有当一辆真正的汽车停在适当的位置足够长的时间时，门才会打开。

说到这里，我们喜欢[Andrew]为这个项目部署 QMC5883X 传感器的方式。小型传感器板和一些吸湿包被放在 Sonoff IP66 防水外壳中，并埋在车道的岩石下。一根标准的 CAT5 电缆被用来将它连接到 ESP8266、继电器和其他各种现在位于闸门控制箱中的设备上。他说，将来电缆可能会进入导管，但目前该系统或多或少地按照他的预期工作。

如果你的房产不够富丽堂皇，不能在前门安装电动大门，我们已经看到了很多项目，这些项目为[简陋的车库门开启器](https://hackaday.com/2019/07/15/the-trials-and-tribulations-of-building-an-iot-garage-door-opener/)增加了一些急需的智能，这可能更符合你的速度。