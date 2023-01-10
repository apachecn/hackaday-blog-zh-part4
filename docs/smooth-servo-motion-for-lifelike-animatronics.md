# 流畅的伺服运动，栩栩如生的电子动画

> 原文：<https://hackaday.com/2021/09/03/smooth-servo-motion-for-lifelike-animatronics/>

制造一个电子动画机器人是一回事，但以栩栩如生的方式制作它却是完全不同的挑战。业余爱好伺服系统对于电子动画来说既便宜又受欢迎，但是仅仅让它以最大速度移动并不是特别逼真。在休息后的视频中，[詹姆斯·布鲁顿]演示了如何用一个简单的电子动画头和几行额外的代码实现自然运动。

很少有自然的身体运动是匀速进行的，它总是在加速或减速。当我们移动头部看周围的东西时，颈部肌肉会在选定的方向上急剧加速，然后在到达终点时逐渐减速。为了在 Arduino/C 代码中做到这一点，为每个主循环指定一个新的伺服中间位置，直到它到达最终位置。中间值是当前位置的 95%和目标位置的 5%之和。这给出了上述自然运动的效果。比率可以改变，以适应所需的速度。

*延迟* 功能通常是新 Arduino 程序员最先学习的计时机制之一，但它不适合这种应用，尤其是当你同时控制多个伺服系统时。相反，*millis*函数用于跟踪主循环中的系统时钟，它以指定的间隔触发位置更新命令。Adafruit 写了一篇关于这种多任务处理方法的优秀教程，[James]就是以此为基础编写代码的。当然，对于已经从事嵌入式编程一段时间的人来说，这应该是旧闻了，但是对于新手来说，这是一个极好的介绍。

和大多数[James]的项目一样，所有的代码和 CAD 文件都是开源的，可以在 [GitHub](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqazYyaW9PX2RES1ViQjV0RUtRdVFQZHBpa1dqQXxBQ3Jtc0trRXNwSXhZR0Nub1lqeVFER1ktR2g0Rl9NTk5uRXktbHNhQUZ2ZFFzSGpJTjFpZ2hZTVhUV1NLZm80VWtDY3BpendhNTZIMmdTQXZhQmk4ZzdqY3hPcVF5czNLYUZVeWV0RVlYcEZVQWd3NnJKMUVsMA&q=https%3A%2F%2Fgithub.com%2FXRobots%2FServoSmoothing) 上获得。他的项目定期在 Hackaday 上亮相，比如他的[单轮平衡机器人](https://hackaday.com/2021/07/24/monowheel-balancing-robot-cant-turn-yet/)和[机械多路翻转点显示器](https://hackaday.com/2021/06/24/mechanically-multiplexed-flip-dot/)。

 [https://www.youtube.com/embed/jsXolwJskKM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jsXolwJskKM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

