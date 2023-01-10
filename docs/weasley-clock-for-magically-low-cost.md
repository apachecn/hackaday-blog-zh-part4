# 韦斯莱时钟神奇的低成本

> 原文：<https://hackaday.com/2022/11/24/weasley-clock-for-magically-low-cost/>

对于那些不熟悉《哈利·波特》这部长篇小说细节的人来说，它确实引入了一些已经深深扎根于集体意识中的想法。除了包含少数几个正确完成的时间旅行实例之一，并介绍了一个相当全面的魔法物理系统，似乎对这里影响最大的一件事是韦斯莱家族的时钟，它显示了几个角色的位置。我们以前见过这些用非魔法的方式建造的，但是这个最新的建造试图降低一个大的价格。

为了做到这一点，该建筑依靠几个低成本的云计算解决方案和智能手机应用程序来解决定位问题。该应用程序名为 OwnTracks，是一款开源的位置跟踪器，可以向许多服务报告数据。[Simon]将 MQTT 数据发送到一个名为 HiveMQCloud 的基于云的解决方案，但原则上你可以将它发送到任何地方。随着位置跟踪的处理，他转向一些非常低成本的 Arduinos 来控制步进电机，这些电机将时钟指针指向表面上的正确位置。

虽然该建筑确实依赖 3D 打印机来完成时钟的一些内部工作，但与其他选择相比，这确实大大降低了成本。特别是与这个韦斯莱家族的时钟相比，它被安装在一个更大的计时设备中，拥有一个像这样的低成本位置跟踪钟面当然是受欢迎的。