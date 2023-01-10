# 对吊扇遥控器进行逆向工程

> 原文：<https://hackaday.com/2020/03/31/reverse-engineering-a-ceiling-fan-remote/>

在寻求家中一切自动化的过程中，你无疑会有一些不是为家庭自动化设计的东西。也许是你的窗户空调，或者是你餐厅的调光器。[Seb]有几个由遥控器控制的吊扇，他想将它们连接到他的家庭自动化系统。通过这样做，[Seb] [很好地概述了如何解决这个问题，以及如何设计 PCB](https://www.youtube.com/watch?v=HGYSuoNjKs0) ，这样他就不会有一个试验板连接到他的遥控器的内部。

为了将他的风扇连接到他使用的家庭自动化系统[家庭助理](https://www.home-assistant.io/)，有几件事情[Seb]需要弄清楚:他需要确定遥控器中的电路是否可以由 5 或 3.3 V 供电，他需要将电路连接到 ESP32 板，他需要弄清楚他是否可以创建一个将电路和 ESP32 合二为一的定制 PCB。该视频介绍了每一个步骤，并展示了每个步骤的发展过程。

视频中有很多信息，所以可能需要放慢一点速度才能看到所有细节。网站上还有一些其他的家庭自动化设备的逆向工程，这里是，或者，你可能想建造自己的[遥控器来控制你的自动化设备](https://hackaday.com/2019/12/26/handheld-mqtt-remote-for-home-automation/)。

 [https://www.youtube.com/embed/HGYSuoNjKs0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HGYSuoNjKs0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

