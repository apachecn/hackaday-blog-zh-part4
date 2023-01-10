# 机器人球弹跳器使用机器视觉停留在目标上

> 原文：<https://hackaday.com/2020/03/05/robotic-ball-bouncer-uses-machine-vision-to-stay-on-target/>

当我们第一眼瞥见[这个球杂耍台](https://electrondust.com/2020/03/01/the-octo-bouncer/)的时候，就瞬间被它的外观所吸引。凭借其机械加工的金属连杆和透明的聚碳酸酯平台，它具有不可抗拒的工业外观。尽管看起来很吸引人，但实际上它更酷。

你可能知道[T-Kuhn]这个名字，也能从他之前的杂耍机器人中感受到“八臂保镖”的根源。早期版本给人印象特别深刻，因为它使用麦克风来听球从平台上反弹回来的乒乒乓乓声，并确定其位置。这个版本走的是光学反馈路线，使用安装在平台下的摄像头，在 Windows 机器上使用 OpenCV 来跟踪球。平台连杆由 150 块 CNC 铝制成，每个臂由 NEMA 17 步进机和行星齿轮箱驱动。运动控制是通过 Teensy，选择其超快的时钟速度，使加速和减速曲线更平滑。在下面的视频中从多个角度观看它的运行。

向[T-库恩]脱帽致敬，他有着出色的身材和令人着迷的球技。他的两个杂耍手都出色地控制住了球；他的机器人抛球器被设计成每次都能把球抛到同一个地方。

 [https://www.youtube.com/embed/lYyAMDYzJQM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lYyAMDYzJQM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

