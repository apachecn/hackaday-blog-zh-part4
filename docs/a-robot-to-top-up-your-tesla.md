# 给你的特斯拉汽车充电的机器人

> 原文：<https://hackaday.com/2021/07/02/a-robot-to-top-up-your-tesla/>

只要你记得加油，晚上给你的车加油而不用去加油站的便利是很大的。你真的不想在匆忙中被一个空电池困住。如果你把健忘算作你的弱点之一，那么[帕特·拉森]的[特斯拉插电机器人](https://www.youtube.com/watch?v=octvXMaTG44)可能是一份方便的保险。

该机器人由一个标准的特斯拉充电插头组成，插头连接到安装在[Pat]车库墙上的 2 轴机械臂上。一切都由运行在 Raspberry Pi 4 上的 Python 脚本控制。在用相机模块拍照后，它使用张量流 Lite 机器学习模型来确定充电口盖上反射器的位置。该平台前后移动以与充电端口对齐，之后它使用特斯拉 API 打开充电端口。然后，它将手臂伸向充电端口，使用超声波近程传感器进行距离控制，并再次使用相机模块和张量流来寻找充电端口附近照亮的特斯拉标志。充电插头是翻转使用一个大型伺服，并在一些最终的位置调整后，它采取了暴跌。虽然机器人不会赢得任何室内设计比赛，但它做得很好，增加了一点便利和内心的平静。

我们见过的其他特斯拉黑客包括[以 6500 美元](https://hackaday.com/2017/09/20/salvaging-your-way-to-a-working-tesla-model-s-for-6500/)建造一辆工作模型 S，使用特斯拉零件将一辆[旧本田变成速度恶魔](https://hackaday.com/2018/03/28/car-revival-according-to-tesla/)，以及可以解锁你的特斯拉的[卡西欧 F-91W](https://hackaday.com/2020/09/04/see-this-casio-watch-it-unlock-my-tesla/)。

 [https://www.youtube.com/embed/octvXMaTG44?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/octvXMaTG44?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

