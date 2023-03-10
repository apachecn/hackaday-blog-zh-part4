# 杂耍机听弹跳来保持球在空中

> 原文：<https://hackaday.com/2018/07/25/juggling-machine-listens-to-the-bounce-to-keep-ball-in-the-air/>

这是一个看似简单的任务:在木制球拍上拍击乒乓球。如此简单，几乎任何人都可以拿起一个球和一个球拍，并做出合理的工作。现在，闭上你的眼睛，试着根据球撞击球拍时发出的声音来做。这有点难，但是这个步进驱动的平台杂耍者泰然自若地完成了任务。

这并不是说[tkuhn]通往下面视频中成品的道路是一帆风顺的。在过去的两年里，他经历了多次迭代，包括一个用光电晶体管围栏包围杂耍平台的版本，以随时跟踪球的位置。这通过一个交叉连杆驱动四个步进电机，在正确的时刻弹出平台以保持球的运动，并在正确的角度将其推回平台的中心。该平台的当前版本取消了光学传感器，代之以四个小型麦克风。麦克风拾取球撞击平台的清晰声音，通过模拟电路处理信号，并在信号超过设定点时使用该信号触发触发器。Arduino 然后测量到达信号之间的时间延迟，计算球在平台上的位置，并通过 PID 环路驱动步进器发出校正反弹。

下面的视频很吸引人，但我们发现自己也想从侧面看一下这个动作。尽管如此，这仍然是一个令人印象深刻的建筑，它让我们想起了我们见过的许多迷宫机器人和 T2 机器人。

 [https://www.youtube.com/embed/0WiGiJk03Q8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0WiGiJk03Q8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [r/arduino](https://www.reddit.com/r/arduino/comments/90xg55/acoustic_location_determination_of_a_bouncing_ball/)