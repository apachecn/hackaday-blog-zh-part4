# 机器学习帮助你在做案头工作时保持体形

> 原文：<https://hackaday.com/2022/04/22/machine-learning-helps-you-get-in-shape-while-working-a-desk-job/>

人类不是生来就要整天坐在电脑前的，但对我们中的许多人来说，这就是我们生活中的大部分时间。当然，我们都知道时不时站起来走动一下，伸展一下肌肉，让血液流动起来是很重要的，但是如果你正在赶时间，很容易忘记这一点。[Victor Sonck]认为他需要一些提醒，以及一些不那么温和的推动，以养成每天快速锻炼几次的习惯。

为此，他设计了一款软件，可以锁定电脑屏幕，只有做五个俯卧撑才能解锁。在他的 Linux 盒子上锁定屏幕就像通过网络发送命令一样简单，但识别俯卧撑是一项更困难的任务，为此[Victor]决定采用机器学习。一个带有摄像头的树莓 Pi 可以做到这一点，但 Pi CPU 有限的处理能力可能不足以处理大量的原始图像数据。

[Victor]因此决定使用 Luxonis OAK-1，这是一款内置机器学习处理器的 4K 相机。它可以运行各种图像识别系统，包括 Blazepose，这是一个预先训练好的模型，可以从图像中识别一个人的姿势。OAK-1 利用这一点，通过 USB 接口向树莓 Pi 发出一组描述人的头部、躯干和四肢位置的坐标。在 Pi 上运行的第二个机器学习模型然后分析这个数据集来识别俯卧撑。

[Victor]的视频(嵌入在下面)是对视频处理的机器学习系统世界的有趣介绍，也是一个很好的实践项目的例子，该项目产生了一个有用的工具。如果你有兴趣了解更多关于小型平台上机器学习的信息，请查看[这个 2020 年 Remoticon 关于微控制器上机器学习的演讲](https://hackaday.com/2020/12/04/remoticon-video-how-to-use-machine-learning-with-microcontrollers/)，或者这个 [2019 年 Supercon 关于在树莓皮上实现机器视觉的演讲](https://hackaday.com/2019/03/01/leigh-johnsons-guide-to-machine-vision-on-raspberry-pi/)。

 [https://www.youtube.com/embed/ZiOr9EdYEeE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZiOr9EdYEeE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

