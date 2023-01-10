# 微型无人机像真正的虫子一样导航

> 原文：<https://hackaday.com/2019/11/06/tiny-drones-navigate-like-real-bugs/>

当谈到机器人导航时，通常的方法是尽可能在技术上先进和“智能”。然而，我们所知的最成功的生命形式遵循一种完全不同的方式。由于感官和认知能力有限，蚂蚁和蜜蜂等无脊椎动物的成功在于大量的合作。来自代尔夫特大学、利物浦大学和奈梅亨大学的联合研究小组决定尝试这种方法，并试验了一种简单的导航技术，让一群微型飞行机器人探索未知的环境。

使用的无人机是现成的带附加板的微型四轴飞行器。传感器包括它的机载 IMU，在[多游侠甲板](https://www.bitcraze.io/multi-ranger-deck/)上用于障碍检测的简单测距传感器，以及在[流量甲板](https://www.bitcraze.io/flow-deck-v2/)上用于跟踪行驶距离的向下指向的光学流量传感器。为了导航，无人机使用了“群体梯度错误算法”(SGBA)。每架无人机在起飞时都有不同的首选飞行方向。当遇到障碍物时，它会沿着障碍物的轮廓前进，一旦路径畅通，它会继续朝着自己喜欢的方向前进。当电池电量下降到 60%时，它会返回到无线归航信标。虽然这种技术可能不是最有效的，但它的主要优势是“轻量级”，足以在廉价的微控制器(本例中为 STM32F4)上实现。完整的研究文章是免费的，是一个信息宝库。

研究人员想到的主要应用是搜索和救援。一群无人机可以探索不稳定或危险的区域，并确定重点救援区域。这可以大大减少救援人员浪费的时间和风险。看到复杂的问题被简单的解决方案解决总是很酷，我们渴望看到事情的发展。休息之后请看视频。

 [https://www.youtube.com/embed/IgMKiIEbfN8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IgMKiIEbfN8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在过去的[年](https://hackaday.com/2013/08/22/crazyflie-control-with-leap-and-kinect/)里，我们已经经历了[疯狂快车](https://hackaday.com/2011/04/29/mini-quadrocopter-is-crazy-awesome/)攻击[时代](https://hackaday.com/2015/07/15/controlling-quadcopters-with-wireless-mouse-dongles/)的[号](https://hackaday.com/2012/04/16/tiny-quadcopter-gets-an-update-on-the-virge-of-flying-without-pc/)，这一次很可能不会是最后一次。

感谢[Qes]的提示！