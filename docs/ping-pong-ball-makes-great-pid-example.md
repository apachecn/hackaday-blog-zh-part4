# 乒乓球是很好的 PID 例子

> 原文：<https://hackaday.com/2019/07/31/ping-pong-ball-makes-great-pid-example/>

在电子领域，控制环路是一种常见的情况，它是某种反馈，驱动系统的输入，例如基于传感器的电机或加热器，以测量位置或温度等信息。你会有一个设定点——无论你想让传感器读取什么——你的工作是调整驱动的东西，让传感器读取设定点的值。这看起来很简单，对吗？看起来确实是这样，但实际上做好它有很多细微差别，通常至少涉及 PID(比例、积分、微分)控制器的某些部分。你可以在数学上陷入困境，试图理解 PID，但[electronio OBS]最近的视频显示了一个非常简单的测试设置[，它清楚地展示了一个 Arduino、一个电机、一个距离传感器和一个乒乓球发生了什么。你可以看下面的视频。](https://www.youtube.com/watch?v=JFTJ2SS4xyA)

想象一下加热一箱水的例子。简单的方法是打开加热器，当水温达到设定值时，关闭加热器。问题是，你可能会超额完成目标。PID 控制器的比例部分只会在水温远低于目标温度时将加热器完全打开。随着水温越来越接近正确的温度，控制器将调低输入——在这种情况下使用 PWM。传感器读数越接近设定值，系统将把加热器调得越低。

对于某些应用程序来说，这已经足够了。但是如果有非常小的误差呢？也许设定点是 90 度，而你是 89.8 度。在比例控制回路中，这种情况不会很快得到纠正，因为由于小误差，加热器不会开得很大。随着时间的推移，循环的组成部分将对小错误做出反应，每次系统处于不正确的状态时都会增加一点点。导数部分则相反。它会影响对突然变化的反应输出，例如冰块落在水箱中。

示例钻机是一个类似跷跷板的平衡木，使用了[许多 3D 打印零件](http://electronoobs.com/eng_arduino_tut100_stl1.php)和一些胶合板。该系统的输入驱动器是一个 RC 伺服系统，可以将跷跷板倾斜到不同的角度。红外传感器确定乒乓球离光束边缘有多远。所有东西都连接到 Arduino，你就有了一个很好的控制器测试平台。

通过设置决定每个动作“强度”的 Kp、Ki 和 Kd 常数来“调整”PID 是很常见的。借助光束，您可以观察调谐如何影响系统。通过设置一个常数为零，你可以关闭算法的这一部分，这是非常有益的，看看方程的每一部分对乒乓球做了什么。

即使你以前使用过 PID，你也会喜欢看这个演示。在教室里会很棒。如果您想查看[温度示例](https://hackaday.com/2018/04/14/pid-control-with-arduino/)，我们已经看到 Arduino 也能做到这一点。PID 是[飞行控制系统](https://hackaday.com/2016/05/18/flying-with-proportional-integral-derivative-control/)和自动平衡机器人不可或缺的组成部分。

 [https://www.youtube.com/embed/JFTJ2SS4xyA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JFTJ2SS4xyA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

