# Remoticon 视频:与 Amith Reddy 一起学习如何黑汽车

> 原文：<https://hackaday.com/2020/12/10/remoticon-video-learn-how-to-hack-a-car-with-amith-reddy/>

不久前，黑客入侵一辆汽车往往涉及字面意义上的入侵。金属板被切割，发动机气缸被钻孔，曲轴被加工以增加活塞行程。这一切都是为了追求从每一滴汽油中榨取最后一盎司的性能，同时以油漆和铬合金的形式表达一点个人情感。

虽然仍有可能——并鼓励——这样黑客攻击汽车，但将发动机控制单元和其他系统纳入我们的游乐设施创造了一个完全不同的汽车黑客选项世界，Amith Reddy 将其提炼到他在 2020 年 Remoticon 上非常受欢迎的研讨会中。在今天的线控汽车中，你可以完成的所有黑客攻击背后的秘密武器是控制器局域网(can)，该网络用于连接现代汽车金属和塑料下面的传感器、执行器和控制器阵列。

 [https://www.youtube.com/embed/NzgvRictI9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NzgvRictI9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Amith 研讨会的主要内容是如何接收和解释 CAN 总线数据包。工具链包括`can-utils`，一组用于检查和操作 CAN 数据包的工具，以及`ICSim`，它以图形方式模拟了一个通用汽车仪表组。使用这些，研讨会参与者能够玩虚拟仪表板，打开和关闭虚拟门，并观察负责这一切的 CAN 数据包在网络中的飞行。

随着基础知识的普及，研讨会转向了 CANbus 黑客攻击的现实世界实施，包括通过汽车的车载诊断(OBD)端口接入网络的工具。这里可能会有重大的挑战，包括使用任何大功率机器时固有的危险。[研讨会页面](https://hackaday.io/project/175126-learn-how-to-hack-a-car-remoticon-workshop)包含开始所需的所有细节，研讨会的视频将带您安全地完成余下的旅程。