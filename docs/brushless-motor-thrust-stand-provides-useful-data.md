# 无刷电机推力支架提供有用的数据

> 原文：<https://hackaday.com/2018/12/16/brushless-motor-thrust-stand-provides-useful-data/>

设计任何形状或尺寸的模型飞机时，了解所选部件的预期性能是很有用的。对于马达和螺旋桨，这可能是困难的。最好是将它们结合起来测试。然而，由于螺旋桨和马达组合的数量可能很多，这样的数据可能很难获得。[[Nikus]认为在内部进行测试会更容易，于是建造了一个测试平台。](https://www.instructables.com/id/Brushless-Motor-Thrust-Stand/)

这一构建中的关键组件是应变仪，它已经与 Arduino 兼容的模数转换器模块结合在一起。[从 Banggood 以不到 10 美元的价格采购，](https://www.banggood.com/HX711-24bit-AD-Module-1kg-Aluminum-Alloy-Scale-Weighing-Sensor-Load-Cell-Kit-For-Arduino-p-1124935.html?p=PW041611183930201706&custlinkid=84569&cur_warehouse=CN)我们不禁认为，2018 年我们过得很轻松。坚固的框架将电机和螺旋桨组合固定在应变仪组件上。ATMEGA328 负责向电机控制器发送命令，读取应变仪结果，并将数据发送到 LCD。

这是一个廉价而有效的构建，解决了一个棘手的问题，对于任何严肃的建模者来说都是一个有用的补充。我们也看到了这一领域的其他方法，[对于那些渴望绘制他们的运动表现数据的人来说。](https://hackaday.com/2016/04/04/automating-rc-motor-efficiency-testing/)休息后的视频。

【感谢 Baldpower 的提示！]

 [https://www.youtube.com/embed/Y8D_425aGxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y8D_425aGxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

