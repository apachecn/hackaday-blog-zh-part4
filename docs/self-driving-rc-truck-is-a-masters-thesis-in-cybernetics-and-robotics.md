# 自动驾驶遥控卡车是控制论和机器人学的硕士论文

> 原文：<https://hackaday.com/2020/10/31/self-driving-rc-truck-is-a-masters-thesis-in-cybernetics-and-robotics/>

遥控汽车是一种有趣的消遣方式，但对于许多黑客来说，将事情发展到下一个阶段需要让汽车自动驾驶。在他的硕士论文中，[Jon]就是这么做的，[建造了一辆自动驾驶的机器人卡车，自信地在他的实验室地板上巡逻](https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2625670)。

该卡车是基于 1/14 比例的田宫底盘，并已由一个小组配备了感应充电系统。在这个平台之上，[Jon]添加了一个 Jetson TX2 作为系统的大脑，将它与 Slamtec RPLIDAR 扫描仪连接起来，以绘制其周围的环境。车上还有一个微型微控制器，用于为驱动卡车的无线电控制硬件合成 PWM 信号，以及一个用于机器视觉的罗技网络摄像头。该卡车能够在多种模式下运行，从完全手动操作到基于激光雷达测绘或基于相机数据控制卡车的人工智能驾驶。这辆卡车被编程为行驶一条包括感应充电板的路线，因此它可以在没有人工干预的情况下保持其功率水平。

这是一个自动驾驶系统的伟大蓝图，而且[Jon]的论文非常详细地介绍了基础层面上的一切是如何工作的([在本页面上以 67 MB PDF](https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2625670) 的形式提供)。出于好奇，他的代码在 Github [上。我们以前也见过类似的项目，](https://github.com/joneivind/Self-Driving-Truck)[像这个机器人用激光雷达导航它的建筑者的房子](https://hackaday.com/2020/09/22/autonomous-rover-navigates-the-house-with-lidar/)。休息后的视频。

 [https://www.youtube.com/embed/N_L3MuPEHa8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/N_L3MuPEHa8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

