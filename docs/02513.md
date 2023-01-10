# 一个宠物机器人，就像波士顿动力公司制造的一样

> 原文：<https://hackaday.com/2019/03/30/a-pet-robot-just-like-boston-dynamics-makes/>

每隔几个月左右，波士顿动力公司的新视频就会在互联网上流传。这是他们的广告，因为除非军方开始购买机械骡子，否则波士顿动力公司很快就会倒闭。你会看到机器人被踢下楼梯，机器人走过门，机器人表现得像狗一样。如果 100 名左右的高技能和受过高等教育的机器人专家、技术专家和其他专家可以在十年内组装一个步行狗机器人，显然一个人就可以在地下室里建造一个。这就是[米沙]正在做的。这是一只令人眩晕的狼，一只机器狼，或狗，或猫，我们实际上不知道，因为还没有皮毛(或头)。但这很有趣。

任何四足机器人的关键部件都是高扭矩、低噪音的伺服电机。这不是一个普通的无刷电机，对于这个应用程序，9 克伺服去垃圾桶。[这意味着定制的马达](https://hackaday.io/project/164175-custom-motor-for-robotics)，或 DizzyMotors。你看到的是一个带有行星齿轮组的大型无刷电机，所有这些都被挤压成一个实际上可以放入机器狼腿关节的东西。

这些电机有一个驱动器，[奇怪的是不被称为令人眼花缭乱的驱动器](https://hackaday.io/project/28512-bldc-motor-driver-for-robotics)，它将 BLDC 变成一个直接驱动的伺服电机。它实际上是一个智能伺服系统，将移动到特定的旋转，通过 RS-485 接收命令，并写回角度位置。它还应用恒定扭矩。当然，下面还有 DizzyMotor 和伺服驱动的视频。

建造一只可以在房子里走动的机器狗是最难的工程挑战之一。你有相当疯狂的运动学，你需要考虑框架的强度，控制系统，最终如何在紧凑的设计中适应一切。这个项目正在击中所有的标记，我们迫不及待地想看到晕狼做一个后空翻或追逐一个球。

 [https://www.youtube.com/embed/yBeU9NSkT58?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yBeU9NSkT58?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/5dqjaBUwD5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5dqjaBUwD5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

