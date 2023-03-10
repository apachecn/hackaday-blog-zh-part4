# 陀螺控制的 RGB 闪光球将点亮你的生活

> 原文：<https://hackaday.com/2018/11/02/gyro-controlled-rgb-blinky-ball-will-light-up-your-life/>

来自 XRobots YouTube 频道的詹姆斯·布鲁顿以他的多部分机器人和角色扮演作品而闻名。不过，偶尔他也会创造一个一次性的建筑。最近，他制作了一个视频，展示如何制作一个 LED 球，这个球根据它的移动而改变颜色。

该项目围绕一系列 3D 打印的“手臂”围绕一个中空的核心，每个手臂都装有一条 APA102 RGB LEDs。Arduino Mega 从 MPU6050 读取方向数据，并根据该输入改变 led 的颜色。Mega 上的两个按钮可以改变 led 改变颜色的方式。Mega，MPU6050，电池和电源电路安装在球的中间。点星带粘在弯曲臂的外侧，布线从点星带的一端开始，向上穿过球的中间列，到达下一个臂的顶部。这意味着更复杂的布线，但允许更容易的 led 编程。

与[詹姆斯的]其他项目不同，这是一个快速的项目，但它是用 Arduino 编程 DotStar LEDs 以及使用加速度计和陀螺仪芯片的一个很好的介绍。如果你想自己创作，代码和 CAD 就在 Github 上。[詹姆斯]以前在网站上有过一些他的项目；看看他的[开放式狗项目](https://hackaday.com/2018/06/11/james-bruton-is-making-a-dog-opendog-project/)，但也有另一个 [blinky ball 项目](https://hackaday.com/2012/04/26/david-hand-soldered-a-blinky-ball-and-you-can-too/)。

 [https://www.youtube.com/embed/DMBejIlcKSM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DMBejIlcKSM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

