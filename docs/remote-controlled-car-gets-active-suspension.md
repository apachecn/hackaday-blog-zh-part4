# 遥控汽车获得主动悬挂

> 原文：<https://hackaday.com/2021/04/14/remote-controlled-car-gets-active-suspension/>

主动悬挂几乎是汽车的圣杯，增加了如此多的性能增益，以至于某些类型甚至被禁止参加 f1 比赛。然而，这并没有阻止它们被用于各种各样的豪华和高性能汽车上，因为它们可以很容易地在飞行中进行调整，以提高舒适度或改善操控性。它们也可以安装在遥控汽车上，如[不确定设计]所示，这款[电子伺服操作的主动悬挂系统用于他的遥控卡车](https://www.youtube.com/playlist?list=PLtkERGXE-7ybFOcPffsLiwgJQ5Sw_unIm)。

四个伺服系统中的每一个都与卡车上现有的 coilover 悬挂系统的安装点相连。这允许伺服系统在卡车移动时改变悬架的定位角度。因此，卡车有一个戏剧性的性能增强，包括更紧密的转弯半径，更稳定，和做甜甜圈的能力。该控制系统运行在带有 ESP32 的 Arduino 上，以实现实时数据流，还包括一个 MPU6050，以监控卡车运动时的车架位置。

这款车有很多改进，尤其是处理所有伺服系统的控制系统。现在它只是被编程为试图保持卡车的车身相对水平，但[不确定设计]计划在未来编程几个额外的控制模式。像这样的系统有很多要考虑的，如果你想适应火箭联盟般的跳跃，甚至更多。

 [https://www.youtube.com/embed/pqRWjGtnvRU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pqRWjGtnvRU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

