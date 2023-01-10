# 用 PX4 飞行控制器操纵滑翔机

> 原文：<https://hackaday.com/2019/03/27/running-a-glider-with-the-px4-flight-controller/>

目前有一些开源的自动驾驶仪可用于四轴飞行器和固定翼飞机。最受欢迎的两个是 ArduPilot 和 PX4，但是这两个都不能用于无动力飞机。尽管如此，[rctestflight]决定进行一些实验，看看 PX4 在控制无人机发射的穿梭滑翔机时会有什么表现。

滑翔机是一个简单的设计，由泡沫板制成，由两个升降副翼控制，并装有第三个伺服系统来处理它从拖车无人机上的释放。它配备了 Pixracer 自动驾驶模块和与地面控制笔记本电脑的 Dragonlink 遥测链接。

最初的测试没有成功，无人机忽略了返回家园的命令，只对航路点做出反应。经过进一步的试验，性能得到了提高。测试和调整是游戏的名字，虽然试图将滑翔机飞到拖车的后面失败了，但总的来说，这个项目显示出了希望。

看到滑翔机在自动驾驶仪的控制下在地图上划出完美的圆圈，令人印象深刻。虽然没有得到官方支持，但[rctestflight]的工作表明，在滑翔机上运行 PX4 是可能的，并取得了一些成功。未来的计划包括气象气球和高空作业，我们迫不及待地想看到结果。

PX4 已经被广泛用于各种项目中，甚至可以用于非常不寻常的飞机。休息后的视频。

 [https://www.youtube.com/embed/YqQr4tHLKOo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YqQr4tHLKOo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

