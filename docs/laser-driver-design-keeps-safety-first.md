# 激光驱动器设计保持安全第一

> 原文：<https://hackaday.com/2022/05/29/laser-driver-design-keeps-safety-first/>

[Les' Lab]的[Les]设计了一款功率高达 10 瓦的激光二极管驱动器，[并决定向我们展示](https://www.youtube.com/watch?v=WQhi3bTNnF4)其工作原理，告诉我们在设计这种驱动器时应该注意的事项，并从总体上谈论激光安全。该设计是基于 LM350A 的可调电流调节器，能够在大约 2 伏的电压下提供高达 10 瓦的功率，这正是他的二极管所需要的。这种晦涩难懂的要求不是普通 PSU 能轻易满足的，这就是为什么需要定制设计的原因。

他告诉我们他是如何提高电流调节电路的稳定性、PCB 设计要求以及为这种驱动器规划用户界面的。然而，这只是战斗的一部分——适当调节电流很重要，但减少意外伤害的可能性更重要。因此，他广泛谈论了在设计驱动电路时要考虑安全问题——使用各种联锁装置，如闭锁继电器电路，以防止它在通电后立即上电。

当然，安全问题超越了驾驶员的特征，[Les]也是如此，认为我们应该知道操作如此功率的激光器需要什么。他解释了为所涉及的波长选择合适的安全眼镜的重要性——各种相关数字的含义，以及如何使用这些数字来选择真正能够保护你在事故中失明的眼镜。把所有东西都固定好也是需要的——你不会希望激光意外地偏离你希望它照射的路径，因为即使是反射也会相当危险。

最后，[Les]展示了驾驶员与激光二极管的结合，并产生了足够的烟雾，我们在法律上有义务认为这是一次“烟雾测试”——一次成功的测试！他对那个二极管有很大的计划，我们迫不及待地想看到他们实现。

[Les]的[YouTube 频道](https://www.youtube.com/c/LesLaboratory/videos)有各种与电子相关的 DIY 制作视频，如果你对激光相关的话题感兴趣，绝对值得一试。我们过去报道过他的一些作品，包括基于[树莓 Pi 的光谱仪](https://hackaday.com/2021/04/23/pi-based-spectrometer-puts-the-complexity-in-the-software/)和[一个简单火花隙的高压开关](https://hackaday.com/2022/03/16/spark-plug-and-plumbing-parts-bring-nitrogen-laser-under-control/)。

 [https://www.youtube.com/embed/WQhi3bTNnF4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WQhi3bTNnF4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

