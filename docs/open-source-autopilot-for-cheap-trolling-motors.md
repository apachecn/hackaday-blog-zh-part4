# 廉价拖曳马达的开源自动驾驶仪

> 原文：<https://hackaday.com/2021/09/24/open-source-autopilot-for-cheap-trolling-motors/>

安静的电动拖曳马达非常适合滑入你最喜欢的钓鱼点，但是如果风和水流在起作用，就需要不断的修正。作为昂贵的商用 GPS 导航拖拽马达的替代物，[AlexAsplund]创造了 [Vanchor](https://vanchor.org/) ，这是一个为廉价拖拽马达添加自动驾驶仪的开源系统。

为了自主控制现成的拖曳电机，[Alex]设计了一个由步进电机驱动的 3D 打印转向单元，以连接到电机垂直轴上方的原始横梁支架上。当电机下降时，拧紧在轴上的轴环将电机锁定在转向装置中。主控制器是一个 Raspberry Pi，它托管一个 WiFi 热点和网络服务器，用于使用智能手机进行控制和配置。使用来自电子罗盘传感器和海洋 GPS 海图绘图仪的导航数据，它可以保持位置，在指定的方向上行驶，或遵循定义的路线。[Alex]还计划添加使用 GPS 模块而不是商用绘图仪的选项。

估计总共 300 美元，包括发动机，这似乎是一个可行的替代商业系统。当然，通过集成开源的 ArduRover 自动驾驶仪，可能会增加更多的功能，正如我们在多艘[自主船只](https://hackaday.com/2021/09/18/solar-powered-autonomous-tugboat-for-rescuing-autonomous-vessels/)上看到的[【rctestflight】所做的](https://hackaday.com/2021/03/11/drone-boat-sails-seattle/)。你也可以使用 [OpenCPN](https://opencpn.org/index.html) 构建自己的[开源绘图仪](https://hackaday.com/2019/11/04/traffic-updates-on-the-seven-seas-open-source-chart-plotter-using-a-raspberry-pi/)，它可以与商业产品相媲美。