# 关注取暖油

> 原文：<https://hackaday.com/2022/11/02/keeping-an-eye-on-heating-oil/>

无论是电力、天然气还是汽油，全世界的能源成本都在上涨。这导致许多人寻找减少能源使用的方法，尤其是在北半球即将进入冬季的时候。俗话说，你不能管理你不能测量的东西，所以[史蒂夫]围绕着监测他家的炉子的燃油液位建立了[这个系统。](https://github.com/tangentaudio/opencv_tank_gauge/wiki)

燃油是一种古老的加热方式，但它在世界上的某些地方相当普遍，并且涉及一个通常位于家庭地下室的大型储罐。由于这项技术太过时了，使用任何现代的东西来与这些系统进行交互并不简单。这个油箱有一个液位计显示它当前的充满百分比。附近安装了一个 Raspberry Pi，它带有一个小型摄像头模块来监控油量计，并运行 OpenCV 来确定当前的燃油油位并报告其结果。

由于大多数燃料箱都隐藏在不方便的位置，这使得检查燃料水平变得轻而易举，并有助于避免在寒冷季节耗尽燃料。[Steve]将这个项目设计成可重复的，即使你的油箱和他的不一样。除了 OpenCV 之外，您还有其他选择；[该油箱使用超声波传感器](https://hackaday.com/2013/12/04/using-ultrasonic-sensors-to-measure-and-log-oil-tank-levels/)直接测量燃油深度。