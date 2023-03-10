# 为快速启动而生的 Pi USB 网络摄像头

> 原文：<https://hackaday.com/2021/06/24/a-pi-usb-webcam-that-was-born-to-boot-quick/>

在商业缩放房间的时代，拥有一个清晰的网络摄像头是向你的宠物猫介绍同事的关键。不幸的是，高质量的网络摄像头已经脱销，自己制作是不可能的。或者是？[Dave Hunt]不这么认为，他想出了使用 Raspberry Pi 的 USB 移动模式通过 USB 传输摄像机数据的主意。然后[Huan Trong]更进一步，把这个项目重新想象成一个可引导的系统映像。结果是 [showmewebcam](https://github.com/showmewebcam/showmewebcam) ，一个树莓 Pi 图像，它可以将您的 Pi 与附加的 HQ 摄像头模块转换为高质量的 usb 摄像头，在 5 秒内启动。

showmewebcam 上的一些项目确实令人惊叹。不仅安装启动迅速，目前的版本只需要 64MB 的微型 SD 卡操作。更重要的是，该项目暴露了相机的设置，如亮度，对比度等。通过 UVC，一种标准的 USB 协议，这样它们可以通过典型的软件应用程序来控制。

这个项目真正令人兴奋的是看到它成形，因为不同的人处理相同的概念，同时参考以前的里程碑。[Dave Hunt]很早就来到现场，他在博客上发布了一篇博文，证实 Pi 确实可以用作 USB 网络摄像头。[Huang Truong]在那个起点上构建，使其成熟为一个可上传的系统映像，随后是[的注释](http://www.tnhh.net/posts/show-me-webcam.html)。现在，通过 Github 上的 showmewebcam，它已经看到了来自十几个人的贡献。它的性能规格正在逐步改进。它有一个详细的 wiki，包含[建议的镜头](https://github.com/showmewebcam/showmewebcam/wiki/Lenses)和[用户贡献的案例](https://github.com/showmewebcam/showmewebcam/wiki/Cases)，让你的第一次网络摄像头构建体验获得成功。

这并不是说其他人没有从他们自己的角度来处理这个项目！对于替代的封装解决方案，看看[Jeff Geerling 的] [采用基于 Pi 的 USB 网络摄像头](https://hackaday.com/2020/11/30/usb-webcams-out-of-stock-make-one-with-a-raspberry-pi-and-hq-camera-module/)。

 [https://www.youtube.com/embed/nH2G16YoBT4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nH2G16YoBT4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

