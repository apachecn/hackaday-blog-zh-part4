# Open Leg——开源机器人腿

> 原文：<https://hackaday.com/2019/09/21/openleg-the-open-source-robot-leg/>

有句老话叫站在巨人的肩膀上，但是用开源的腿这样做怎么样？好吧，至少你的机器人可能会这样做，这要感谢 [OpenLeg](https://github.com/JoeyByrnes/OpenLeg) ，一个新的用于建造机器人腿的开源项目。由[乔伊·伯恩斯]创建，它最初是伊利诺伊大学一门课程的高级项目。这个想法是创造一条机器人腿，其他人可以用它来建造四条腿的机器人，可以在附近漫步，就像[波士顿动力](https://hackaday.com/2013/10/05/boston-dynamics-takes-wildcat-outside/)建造的那些一样。

这个项目有一个良好的开端:乔伊制作的样本视频显示，OpenLeg 的原型可以产生各种各样的动作，从字面上的拳击动作到更传统的步行步态。它大部分是 3D 打印的，有一些碳纤维增加了强度。腿由一个为电动滑板设计的大型 50 千伏电机驱动，该电机由一个 [ODrive](https://odriverobotics.com/) 控制器驱动，该控制器处理驱动这样一个大型电机的大部分复杂性，并处理运动学和其他复杂的东西。这个想法是，你最终可以把这个设计插入到你自己的机器人中，用几行 Python 语言就能让它行走，但这还有一段路要走。

我们最近已经看到了很多四足机器人项目，从詹姆斯·布鲁顿的 OpenDog 到加州大学洛杉矶分校的罗梅拉的 T2，但是像这样的项目越多越好。尤其是那些采用更加模块化方法的项目，这样你就可以挑选适合自己的莎拉·寇娜狩猎设备。

 [https://www.youtube.com/embed/aXOSeKpADnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aXOSeKpADnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

