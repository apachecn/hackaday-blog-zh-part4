# Nvidia Jetson 机器人通过 Isaac 软件工具获得领先优势

> 原文：<https://hackaday.com/2019/06/01/nvidia-jetson-robots-get-a-head-start-with-isaac-software-tools/>

我们生活在一个激动人心的机器智能时代。在过去的几个月里，已经推出了几款神经网络处理器产品，价格在业余爱好者的承受范围之内。尽管硬件可能令人兴奋，但他们仍然需要软件才能发挥作用。Nvidia 并不满足于他们令人印象深刻的 Jetson 硬件，而是创建了一个软件框架，以加速在他们周围建造机器人。任何愿意创建 Nvidia 开发者账户的人现在都可以使用 [Isaac 机器人引擎](https://developer.nvidia.com/isaac-sdk)框架。

Isaac 最初是在大约一年前作为 Jetson Xavier 硬件捆绑包的一部分推出的。但是 1，299 美元的开发套件价格标签使我们许多人都买不起。现在我们可以花大约 100 美元买一辆[杰特森纳米。对于熟悉](https://hackaday.com/2019/03/18/hands-on-new-nvidia-jetson-nano-is-more-power-in-a-smaller-form-factor/)[机器人操作系统(ROS)](https://hackaday.com/2018/05/31/modular-robotics-made-easier-with-ros/) 的人来说，萨克看起来会非常熟悉。他们都致力于让机器人软件像连接普通模块一样简单。Isaac 中许多被称为 GEMS 的模块都是根据 Nvidia Jetson 硬件的优势量身定制的。除了那些模块和它们协同工作的方式，Isaac 还包括一个模拟器，用于在虚拟世界中测试机器人代码，类似于 ROS 的 [Gazebo](http://gazebosim.org/) 。

虽然 Isaac 可以在任何具有 Nvidia Jetson 大脑的机器人上运行，但有两种参考机器人设计。卡特是更昂贵和强大的商用机器，依靠赛格威汽车、激光雷达环境传感器和杰特森泽维尔。我们更感兴趣的是 [Kaya](https://docs.nvidia.com/isaac/isaac/apps/tutorials/doc/assemble_kaya.html) (如图)，这是一个 3D 打印的 DIY 机器人，在 Dynamixel [串行总线伺服系统](https://hackaday.com/2018/07/05/wrangling-rc-servos-becoming-a-hassle-try-serial-bus-servos/)上滚动。Kaya 使用英特尔 RealSense D435 深度摄像头感知环境，并使用 Jetson Nano 作为大脑。总的来说，硬件和软件产品是探索智能自主机器人的一个有能力和功能的包。

有点令人失望的是，Nvidia 决定创建自己的专有软件框架，重新发明许多轮子，而不是为 ROS 做出贡献。虽然有一些非常吸引人的功能，如 WebSight(一种基于浏览器的检查和调试工具)，但乍一看，Isaac 似乎与 ROS 没有本质上的区别。开源社区已经开始为 Jetson 硬件创建 ROS 节点，但专门在 Nvidia 生态系统中工作或面临上市时间截止日期的人会喜欢选择像 Isaac 这样的预打包解决方案。