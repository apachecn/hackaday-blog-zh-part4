# 机器学习给了猫多一种控制人类的方式

> 原文：<https://hackaday.com/2022/08/26/machine-learning-gives-cats-one-more-way-to-control-their-humans/>

对于那些选择让他们的猫过上或多或少自由放养生活的人来说，通常有两种选择。第一，你可以扮演仆人的角色，每当猫想从他们最近的杀鸟之旅中回到屋里时，你就跑向门口。或者两个，装一个猫门，让它们来去自由，有时嘴里还会叼着给你的“礼物”。正面你赢，反面你输。

不过，还有另一种方法:让猫要求被放回去。这就是[网球史密斯]对这个机器学习小猫门铃采取的方法。它基于一个住在房子里的树莓 Pi 4 和前门外的 USB 麦克风。Pi 使用 Tensorflow Lite 对它在外面听到的声音进行分类，当其中一个声音符合猫的喵喵声时，就会向 AWS Lambda 发送一条消息。从那里发送一条短信来提醒[网球]这只猫准备好回来了。

这个项目的 repo 中包含了大量有用的信息，包括让 Amazon Web Services 在 Pi 上工作的分步说明。如果你是一个养狗的人，不要害怕:从喵喵声变成狗吠声就像调整一行代码一样简单。如果你不想对猫唯命是从，但仍想避免地毯上出现猎物事件的证据，[机器学习也可以帮助你做到这一点](https://hackaday.com/2019/07/01/ai-recognizes-and-locks-out-murder-cats/)。

[通过[汤姆的硬件](https://www.tomshardware.com/news/raspberry-pi-cat-doorbell)