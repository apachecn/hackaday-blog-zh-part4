# 追踪蚂蚁并用激光杀死它们

> 原文：<https://hackaday.com/2019/10/05/tracking-ants-and-zapping-them-with-lasers/>

由于神经网络和机器学习算法的奇迹，现在有可能做一些曾经被认为用计算机极难实现的事情。这是正确的技术和大量计算能力的结合，使这种壮举成为可能，罗伯特·邦德的蚂蚁消灭项目就是一个很好的例子。

该项目基于 NVIDIA Jetson TK1，这是一个将现代 GPU 的处理能力引入嵌入式平台的系统。它装有一个 USB 摄像头，用来扫描蚂蚁的视野。一旦被探测到，多亏了一点 OpenCV 的魔力，昆虫的坐标被传送到激光系统。双步进电机用于旋转反射镜，反射镜引导 5 mW 红色激光照射目标。如果你正在考虑做类似的事情，我们强烈推荐[使用检流计来引导激光](https://hackaday.com/2018/02/15/laser-galvo-control-via-microcontrollers-dac/)。

如果安装一个更强大的激光，这样的系统可以很容易地蒸发蚂蚁，但出于安全考虑，[罗伯特]决定避免这样做。此外，气味不会很好，而且没有人希望厨房地板上到处都是烧焦的昆虫残渣。我们也见过人工智能做类似的工作——[比如出于安全原因检测淘气的猫](https://hackaday.com/2019/07/01/ai-recognizes-and-locks-out-murder-cats/)。

 <https://hackaday.com/wp-content/uploads/2019/09/intro.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2019/09/intro.mp4](https://hackaday.com/wp-content/uploads/2019/09/intro.mp4)