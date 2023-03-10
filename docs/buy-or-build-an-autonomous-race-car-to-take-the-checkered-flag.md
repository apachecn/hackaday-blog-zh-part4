# 购买或建立一个自主赛车采取方格旗

> 原文：<https://hackaday.com/2018/11/30/buy-or-build-an-autonomous-race-car-to-take-the-checkered-flag/>

将自动驾驶汽车放在公共道路上需要大量资源，超出了我们的大多数能力。但是，我们可以通过改装遥控玩具汽车，在更小的范围内探索所有相同的一般概念，只受我们个人预算和技能水平的限制。对于我们这些对软件感兴趣和专业知识的人来说，亚马逊网络服务刚刚推出了 [AWS DeepRacer](https://aws.amazon.com/deepracer) :一个探索自动驾驶汽车上机器学习的完整包。

在硬件层面，规格表听起来好像他们已经将他们的 [AWS DeepLens](https://aws.amazon.com/deeplens/) 机器视觉计算机固定在 1/18 比例的怪物卡车底盘上。但硬件只是冰山一角。DeepRacer 背后的软件是 [AWS RoboMaker](https://aws.amazon.com/robomaker/) ，这是一套将 AWS 应用于机器人开发的工具。从在 AWS 上运行数字模拟到在 AWS 上训练神经网络，无所不包。对机器学习了解不够？没问题！亚马逊也刚刚向世界开放了他们的内部[培训课程](https://aws.amazon.com/blogs/machine-learning/amazons-own-machine-learning-university-now-available-to-all-developers/)。为了鼓励参与，亚马逊正在运营一个 DeepRacer 联盟，在世界各地的 AWS 峰会活动中，以数字在线和物理方式进行比赛。在本周的再发明会议上，他们确实给了我们很多机会。

[![](img/ab437fde1909033b3d6315bf52e5f313.png)](https://hackaday.com/wp-content/uploads/2018/11/donkey-car-graphic_orig.jpg) 但也许有人宁愿不用亚马逊，或者宁愿自己造硬件，或者[自己办比赛](https://diyrobocars.com/)。幸运的是，亚马逊不是唯一的游戏，仅仅是一个现有领域的最新进入者。DeepRacer 的联赛前身是 [Robocar 拉力赛](https://aws.amazon.com/blogs/machine-learning/congratulations-to-the-winners-of-the-reinvent-robocar-rally-2017/)，DeepRacer 本身沿用[驴车](http://www.donkeycar.com/)。我们[在湾区 Maker Faire 2017](https://hackaday.com/2017/06/06/self-driving-rc-cars-with-tensorflow-raspberry-pi-or-macbook-onboard/) 上首次看到的一个自己动手的自主赛车平台，驴车已经建立了自己的[文档](http://docs.donkeycar.com/)和软件工具，包括一个[模拟器](http://docs.donkeycar.com/guide/simulator/)。默认的驴车代码对于汽车来说是相当具体的，但是建造者当然可以自由地使用一些更通用的东西，比如开源的[机器人操作系统](http://www.ros.org/)和[露台机器人模拟器](http://gazebosim.org/)。(这是 AWS RoboMaker 的基础。)

因此，如果目标是开始小型自动驾驶汽车比赛，我们可以选择购买预建硬件或享受构建自己的硬件的灵活性。无论如何，这只是另一个例子，说明为什么这是进入神经网络的好时机，不管有没有像亚马逊这样的公司想办法赚我们的钱。当然，这不是唯一一个试图围绕现有开源项目探索的想法建立业务的亚马逊项目。我们刚刚[谈到他们的自动气象站地面站](https://hackaday.com/2018/11/27/amazon-creates-distributed-satellite-ground-stations/)提供覆盖类似地面(天空？)作为我们 2014 年黑客日的获奖者 [SatNOGS](https://hackaday.io/project/1340) 。