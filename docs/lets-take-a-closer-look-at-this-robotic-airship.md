# 让我们仔细看看这个机器人飞艇

> 原文：<https://hackaday.com/2020/07/22/lets-take-a-closer-look-at-this-robotic-airship/>

这不是一个气球，无论它的外表看起来多么闪亮。这个由奥克兰大学机械工程研究小组[新灵巧](http://newdexterity.org/)创造的[微型室内机器人飞艇](https://hackaday.io/project/171797-a-helium-based-affordable-robotic-airship)是一个非对称系统，正在试验开源氦基飞艇的可能性。

为什么是氦气飞艇，而不是固定翼飞机？该小组希望试验轻于空气(LTA)旅行的优势，即更高的机动性和更宽松的路径规划约束。此外，LTA 飞艇具有较少的视野障碍和较少的运动问题。虽然无人驾驶飞行器(UAV)可能能够在一个地方悬停，但它们的升力是由转子推力产生的，这在几分钟内就会迅速耗尽它们的电池。LTA 飞艇可以悬停更长时间。

该设计是出于教育和研究目的而创建的，重点关注制造平台的财务可行性、材料的环境影响以及氦气通过气球状外壳的损失。通过测量这些参数，研究人员能够研究环境的影响，如室内商业气球的成本和气球材料的机械性能。

飞艇吊舱是以模块化的方式设计和 3D 打印的，然后用 Velcro 贴在信封上。座舱相对于水平对称的放置是为了飞行稳定性，对几种构型的侧旋翼角度进行了试验。

该小组开源了他们的 CAD 文件和 ROS 接口来控制飞艇。他们主要使用现成的组件，如 Raspberry Pi 板、螺旋桨、DC 单刷电机驱动器载体和 LiPo 电池，平台总成本为 90 美元，另外还有 20 美元用于气球和初始氦气填充。价格堪比像 Blimpduino 2.0 这样的室内软式飞艇的成本。

你可以看看下面完成的飞艇，团队展示了它基于胡萝卜追逐寻路算法的路径跟踪能力。如果你有兴趣了解更多关于建造轻于空气的交通工具的知识，请查看贝尔格莱德 hack aday 的[Sophi Kravitz 的]软式飞艇演讲。

 [https://www.youtube.com/embed/TQCl9RjmE-4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TQCl9RjmE-4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)