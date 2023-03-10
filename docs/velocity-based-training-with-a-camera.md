# 基于速度的训练，带摄像头

> 原文：<https://hackaday.com/2020/03/08/velocity-based-training-with-a-camera/>

在重量训练的世界里，现在的流行词是 VBT，或基于速度的训练。这涉及到使用传感器来测量重物在每次重复运动时的速度和位置，从而为运动员提供即时反馈，并收集信息，使他们能够在日常训练中发挥作用。通常涉及的传感器可能是加速度计，但[Kris]采取了不同的策略[使用网络摄像头和机器视觉来完成相同的工作](https://hackaday.io/project/170185-optical-barbell-tracker-for-vbt-strength-training)。

杠铃的末端附有一个绿色圆盘，软件会跟踪它并测量速度。当重复的速度下降到预设水平以下时，它会发出警告，告诉运动员在将自己推得太远之前停止他们的设置。在引擎盖下是一个 Python 脚本和 OpenCV，他的 GitHub 库中的文章[带我们通过它的相机校准来消除失真和设置的影响。图像内的所有距离校准都是通过已知大小的绿色圆盘进行的，允许软件精确地绘制它行进的距离。](https://github.com/kostecky/VBT-Barbell-Tracker)

我们以前没有见过机器视觉方法进行负重训练，但[我们见过一种使用加速度计的方法](https://hackaday.com/2012/03/25/weightlifting-coach-will-nag-you-about-your-form-at-least-until-the-batteries-run-dry/)。也许这个项目会重新点燃人们对这个领域的兴趣。