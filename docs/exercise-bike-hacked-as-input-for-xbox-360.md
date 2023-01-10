# 健身车被黑为 Xbox 360 的输入

> 原文：<https://hackaday.com/2022/01/25/exercise-bike-hacked-as-input-for-xbox-360/>

如果你喜欢玩侠盗猎车手，你应该很熟悉在开车时踩下加速和刹车的扳机。[David Programa]认为这太简单了，于是开发了一个系统，让他可以在虚拟世界中自由行走。

该设备依赖于基于飞轮的健身车，飞轮上放置了六块磁铁，每旋转六次就会触发一个簧片开关。额外的磁铁使系统在低速时有更好的分辨率。霍尔效应传感器将是一种更可靠的方式来建立这种长期生存，但簧片开关确实有效。它与去抖电路配合使用，以保持输出干净。Raspberry Pi 投入使用，运行 Python 程序来读取由簧片开关激活的 GPIO 引脚，计数脉冲以确定踩踏的速度。

Xbox 360 控制器中使用的触发控制是一个电位计，根据其位置产生不同的电压，使其可以作为模拟加速器输入。0 伏对应于无输入，而当触发器完全按下时，读数为 3.3 伏。Raspberry Pi 通过其 PWM 输出来模拟这一点，并与低通滤波器配合使用，以创建相关电压来注入通用 Xbox 360 控制器上的触发输入。

虽然这比简单地使用一个普通的控制器不太实际，但踏板控制确实可以让你在玩侠盗猎车手时得到很好的锻炼。一些更激烈的追逐任务应该是让你心跳加速的好方法，这是一件好事。

具有讽刺意味的是，这个系统只适用于游戏中的汽车和摩托车。《侠盗猎车手》中的自行车是通过踩踏 A 按钮来控制的。或者，你可以考虑在任天堂 Switch 上用类似的系统[玩马里奥赛车。休息后的视频。](https://hackaday.com/2021/02/08/this-joy-con-grip-steers-to-its-way-to-sweaty-victory/#more-460332)

 [https://www.youtube.com/embed/jm95aeSz9Fg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jm95aeSz9Fg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢赞·阿特金斯的提示！]