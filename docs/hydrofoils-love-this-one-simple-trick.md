# 水翼艇喜欢这个简单的技巧

> 原文：<https://hackaday.com/2022/03/04/hydrofoils-love-this-one-simple-trick/>

今年早些时候，[rctestflight]创造了一个活跃的水翼艇遥控飞行器，但发现实际性能非常缺乏。对他和我们来说幸运的是，他继续调整它，一次调整突然把它从噩梦变成了梦。

这个调整就是增加了 ArduPilot 的飞机模型。这个设计有三个伺服系统，每一个驱动三个浮筒下面的一个箔片的角度。这艘船靠安装在顶部附近的一些螺旋桨推进。如果你很了解 ArduPilot，你会注意到现役水翼船没有出现在[支持平台](https://ardupilot.org/copter/docs/common-all-vehicle-types.html#common-all-vehicle-types)的列表中，你是对的。[rctestflight]指出，这三个伺服系统实际上在水下起到了飞机的作用。前面两个是副翼，后面一个是电梯，所有的事情 ArduPilot 都知道如何用一个严格控制的回路来处理，除了一件事；没有高度数据。

所以他偷了一个他早先为他的地面效应飞机开发的技巧[，用一个距离传感器让 ArduPilot 知道如何调整事情。他使用了声纳传感器而不是激光雷达，因为它在水中工作得更好，当他在湖上使用它时，他惊喜地发现它的工作非常棒。主动稳定的最初目标是让 efoil 对波涛汹涌的水域免疫，我们很遗憾地说，它没有达到那个崇高的目标。单个声纳传感器漂亮地跟随它前面的波浪，但不能处理扔向它的复杂波浪。也许某种传感器融合算法可以提供必要的数据，以实现真正的弹性。但我们喜欢看箔片滑过水面，很难记住它是在积极地飞行，而不仅仅是那样漂浮。](https://hackaday.com/2021/10/10/autonomous-ground-effect-vehicle-demonstrator-aims-to-speed-up-maritime-shipping/)

其他人已经尝试过 3D 打印水翼船，但是失败了，而 T2 已经成功了。我们喜欢[rctestflight]回来结束战斗，带走冠军。休息后的视频。

 [https://www.youtube.com/embed/HufHeNmxock?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HufHeNmxock?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

