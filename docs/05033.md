# 人工智能比你先知道球是否在目标上

> 原文：<https://hackaday.com/2019/12/10/ai-knows-if-the-pitch-is-on-target-before-you-do/>

投球是关于准确性和速度的。目标是一个快速的球，允许投手三振击球手。[[Nick Bild]创造了一个人工智能系统，它可以根据摄像头的反馈来确定球在飞行中的轨迹。](https://github.com/nickbild/tipper)

该系统使用 NVIDIA Jetson AGX Xavier，配有一个以 100FPS 运行的 USB 摄像头。Nerf 网球发射器用于向击球手发射球。一旦被触发，人工智能就使用相机捕捉飞行中的球的两个连续图像。这些图像被输入到一个卷积神经网络(CNN)中，软件确定球是朝着好球区前进，还是偏离目标。它利用这些信息分别点亮绿色或红色 LED 来提醒击球手。

虽然这样的系统不太可能很快出现在职业棒球比赛中，但它显示了神经网络系统快速有效地分析数据的强大能力，而这些方法对于人类来说根本不可能。[Nick]的未来目标包括在更快的硬件上运行该系统，并扩展它以确定诸如旋转和在好球区内更精确定位的效果。

我们已经看到 CNN 做了一切事情，从[给西红柿命名](https://hackaday.com/2018/04/26/neural-network-names-nightshades/)到[寻找停车位。](https://hackaday.com/2019/02/04/sudo-find-me-a-parking-space-machine-learning-ends-circling-the-block/)休息后的视频。

 [https://www.youtube.com/embed/dkE9XCBSyhw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dkE9XCBSyhw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

