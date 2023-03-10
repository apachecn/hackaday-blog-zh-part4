# 使用 ESP32 实现廉价的增强现实

> 原文：<https://hackaday.com/2020/12/31/augmented-reality-on-the-cheap-with-esp32/>

增强现实(AR)技术没有像 VR 一样受到关注，在开源开发和可访问性方面严重滞后。对此感到沮丧的是，[Arnaud Atchimon]创造了一款开源、低成本的 AR 耳机，任何人都可以在家里制作，并作为进一步开发的平台

[Arnaud]对 [Tilt Five](https://hackaday.com/2019/09/25/tilt-five-a-fresh-take-on-augmented-reality-tabletop-gaming/) AR 护目镜印象深刻，但这种尖端硬件的价格让大多数人都买不起。相反，他围绕 3D 打印框架、ESP32、廉价液晶显示器和一副太阳镜的镜片设计并制造了自己的产品。电子设备水平包装在框架的顶部，显示器向下指向一对倾斜的镜子，镜子将图像反射到太阳镜镜片上并进入用户的眼睛。[Arnaud]测试了许多不同的镜片，发现带有轻微弯曲的薄镜片效果最好。ESP32 实际上并不运行主要软件，它只是处理在液晶显示器上显示图像。这些图像是由运行软件的计算机发出的。除了显示图像，该软件还可以集成安装在护目镜上的 MPU6050 IMU 和 ESP32 摄像头模块的输入。这使得图像可以随着护目镜的移动而改变视角，并识别环境中的人脸和 AR 标记。

所有的设计文件和软件都可以在 GitHub 上获得，我们退出来看看这个项目的进展。我们已经看到了另一副价格实惠的[增强现实眼镜，它使用智能手机作为显示器](https://hackaday.com/2019/02/18/immersive-augmented-reality-on-a-budget/)，但似乎以前使用的耳机已经不再可用。

 [https://www.youtube.com/embed/_ARUbvlfMmw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_ARUbvlfMmw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

