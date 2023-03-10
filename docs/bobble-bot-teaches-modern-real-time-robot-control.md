# Bobble-Bot 教授现代实时机器人控制

> 原文：<https://hackaday.com/2019/11/07/bobble-bot-teaches-modern-real-time-robot-control/>

Bobble-Bot 使用标准的倒立摆问题[来教授现代机器人控制](https://hackaday.io/project/164992-bobble-bot)使用 Raspberry Pi、RT-Linux 和 ROS。

我们对这个项目的打磨和设计工作印象深刻，它入围 2019 年 Hackaday 奖的决赛也就不足为奇了。 Bobble-Bot 是一个头重脚轻的机器人，坐在两台 BLDC 汽车上。操作的大脑是运行实时 Linux 和 ROS 的 Raspberry Pi。这允许机器人以可预测的方式对其输入做出响应，并且也允许比常规内核更多地控制线程优先级。在过去，我们已经看到这些倒立摆机器人大多运行在微控制器上，正是因为这个原因，所以看到它跳到 Linux 上很酷。

机械机器人可以在任何消费级打印机上打印和组装。我们真的很欣赏小细节，如确保一个螺钉大小可以用来组装整个机器人，消除了对多种工具的需求。

他们也有一个模拟器，机器人的软件是内置的。这是一个重要的时刻，真实世界的行为最终与模拟的性能相匹配。事实上，如果你对 Bobble-Bot 感兴趣，你可以在承诺建造整个东西之前在模拟中尝试一下。

这个项目对任何黑客来说都是一个有趣的构建。当我们在大学学习控制的时候，我们希望有一个像这个一样精致和现代的项目。休息后视频介绍它。

* * *

 [https://www.youtube.com/embed/E5AWNA60c6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E5AWNA60c6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)