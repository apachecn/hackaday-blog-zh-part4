# 网格上的微电池

> 原文：<https://hackaday.com/2020/03/27/microbatteries-on-the-grid/>

不是每个人都有 6500 美元来购买特斯拉 Powerwall(这是一个较低的估计)，但如果你想为你的房子带来电池存储的好处，那么[Matt]的模块化“微型电池”存储系统可能正合你的胃口。有了随用随建的模式，[几乎任何电池都可以放在电网上](https://hackaday.io/project/170506-networked-home-battery)，以便开始储存来自小型太阳能装置或其他电源的电力。

该系统的工作方式与任何其他电池安装方式相同。当需求较高时，一系列微型逆变器开启并向电网输送电力。当需求低时，电池充电。这种设置与消费级系统的主要区别在于，这种系统是高度模块化的，每个模块都通过网络连接在一起，以提高整个系统的效率。这一切都与管理整个设置的 Raspberry Pi 联系在一起。

虽然[所有的软件都可以用来设置这一点](https://github.com/Audio-Injector/RaspberryPi.buildroot.external/tree/BatteryController)，但不言而喻的是，使用主电源工作是危险的，此外，你还需要能够与电网匹配相位角的逆变器、处理反向功率流的电表、愿意接受电力的电力公司，以及一些建筑规范法规。如果你没有把这些都集中起来，[你可能想脱离电网，而不是](https://hackaday.com/2020/01/04/datacenter-ups-heads-home-for-off-grid-power-solution/)。