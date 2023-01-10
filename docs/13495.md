# 摩托车电压调节器使用 MOSFETs

> 原文：<https://hackaday.com/2022/04/29/motorcycle-voltage-regulator-uses-mosfets/>

就摩托车的普遍程度而言，它们的设计和零件往往比轿车和卡车的差异更大。有时这对车手有利，就像本田试验安全气囊或自动变速器。有时它更有问题，像某些美国品牌坚持从 40 年代的推杆发动机设计。而且有时候就是很烦人，比如使用便宜的稳压器经常出故障，表现很差。[fvfilippetti]厌倦了在他的摩托车上处理这个问题，[所以他用 MOSFETs 代替](https://fvfilippetti.wordpress.com/2022/04/28/motorcycle-mosfet-voltage-regulator/)制造了一个定制的电压调节器。

现代汽车交流发电机即使在怠速时也能产生可用的电压，而小型或老式的摩托车交流发电机通常不能。相反，他们依赖于一个更简单但不太可靠的调节器，通常不超过一系列二极管，但只能在电机高速运行时向电气系统输送能量。为了改进这种设计，[fvfilippetti]从 MOSFETs 开始设计了一种开关稳压器，其中有一些有趣的设计考虑。它能够接受 20V 至 250V 之间的输入电压，并提高摩托车使用现代高功率灯的能力，以及为手机等设备充电的能力。

在下面的视频中，电路中增加了一个 LED，以提供调节器正常工作的视觉指示。对于以前在老式自行车上用过整流器或二极管式调节器的人来说，这无疑是一个受欢迎的构造。车辆交流发电机本身也是有趣的动物，而且[它们不仅仅可以用来驱动摩托车的电气系统](https://hackaday.com/2021/01/24/an-alternator-powered-electric-bicycle-gives-rotor-magnetic-field-insight/)。

 [https://www.youtube.com/embed/VHeovCcBAtE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VHeovCcBAtE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

