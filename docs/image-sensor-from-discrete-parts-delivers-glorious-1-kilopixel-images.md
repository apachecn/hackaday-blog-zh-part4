# 来自分立器件的图像传感器提供出色的 1 千像素图像

> 原文：<https://hackaday.com/2019/12/30/image-sensor-from-discrete-parts-delivers-glorious-1-kilopixel-images/>

很有可能此时你身边至少有一个数字图像传感器，可能触手可及。数码相机的普及是因为这些传感器已经变得非常便宜，并且很容易集成到各种设备中。那么，世界上为什么会有人想用分立零件制造一个比普通智能手机摄像头差 12000 倍的图像传感器呢？因为，为什么不呢？

[肖恩·哈金斯]最初开始这个项目是作为一个数码针孔摄像机，这就是为什么它被称为[“数码暗箱”。](https://github.com/IdleHandsProject/diycamera)我们的想法是构建一个 32×32 的光电传感器阵列，并仅使用一个针孔将光线聚焦在其上，但事实证明这在光学上很困难，因为小孔径大大减少了照射到阵列上的光线量。不过，传感器才是有趣的地方。[Sean]将 1，024 个 ALS-PT19 表面贴装光电晶体管与两个 32 位模拟多路复用器一起焊接到定制 PCB 上。微控制器驱动多路复用器依次选择每个像素，一次选择一行和一列。扫描一个阵列需要整整五秒钟，所以拍一张照片让人回想起摄影早期常见的长曝光。当然，这只是一个 1 千像素的图像，但它是有效的。

[Sean]这个项目已经酝酿了一段时间——事实上，他用于摄像机的多路复用器在 2018 年作为一个独立的项目出现。我们很高兴地看到，他得到了其余的建设，即使与回收镜头，他使用。人们想知道[一个 3D 打印的透镜](https://hackaday.com/2014/12/13/3d-printed-lenses-open-up-possibilities/)如何在传感器前工作。

 [https://www.youtube.com/embed/PaXweP73NT4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PaXweP73NT4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

