# 用于微小物体的 3D 扫描仪使用蓝光部件

> 原文：<https://hackaday.com/2019/10/30/3d-scanner-for-tiny-objects-uses-blu-ray-parts/>

有很多不同的方法来构建 3D 扫描仪，摄影测量是一种特别容易实现的方法。这包括从不同角度拍摄一系列照片来构建模型的几何形状。如果你想用小东西来做这个，不用相机，用显微镜代替就行了！瓢虫就是这么做的。

这是一个非常黑客风格的 3D 扫描仪。移动样本的 X-Y 平台来自 KES-400a 蓝光驱动器，从最初的“胖”Playstation 3 中抢救出来。然后使用来自同一驱动器的光学拾取器的线性步进电机创建 Z 轴。旋转步进电机被添加到 Z 轴上，以允许样品旋转。这一切都结合了一个基本的 USB 显微镜来拍摄图像，以及一个树莓 Pi 来处理运行所有步进电机和一些附加驱动板。

[NoseLace]使用该设备创建昆虫的 3D 模型，但它也可以用于其他小物体。这种方法的好处是它创建了 3D 模型和必要的纹理。如果你想亲自尝试，有很多开源工具可供使用。休息后的视频。

 [https://www.youtube.com/embed/0HFc_KZVVn0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0HFc_KZVVn0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

