# 苏联超 8 相机隐藏树莓派零

> 原文：<https://hackaday.com/2021/05/04/soviet-super-8-camera-hides-raspberry-pi-zero/>

几年前，[夏比尔·苏维萨雷塔]突然想到，他想在经典的 Super 8 相机中安装一个现代的数字图像传感器，但他不想在这个过程中破坏一个华丽的复古硬件。经过一番研究，他发现了一款为 1980 年莫斯科夏季奥运会制造的出口版 Avrora 相机，价格便宜。他认为没有人会错过一台带有实用美学的相机，这种美学你会认为是苏联时代的消费科技产品，于是他开始把一个树莓派塞进胶卷盒里。

在这个项目的 Hackaday.io 页面上，[Xabier]解释了一些使这个项目具有挑战性的光学特性。具体来说，官方 Raspberry Pi 相机模块使用的微型传感器远远小于相机设计的 8 mm 胶片。因此，当传感器放置在原始胶片的适当焦距时，图像会被大幅裁剪。正如你在下面的视频中所看到的，这给人的印象是一切都是用相当紧凑的变焦拍摄的。

为了进行这种修改，[Xabier]首先必须将 Pi 相机的传感器从原始光学系统中解放出来，然后小心地将其安装在 Avrora 上的正确位置。为了确保对准，他在固定传感器的环氧树脂固化时，观看了摄像机的实时画面。这让他在一切还没有凝固之前，就可以稍作调整。有了传感器，他只需将 Pi 零和电池组塞进胶卷盒，并将原始相机触发器连接到 GPIO 引脚，这样他就可以在软件中读取它。

考虑到一些摄影师为了让他们的老式相机适应数码相机付出了令人难以置信的努力，这种简单的方法令人耳目一新。最终的视频可能达不到现代标准，但对于这样的项目来说，这才是重点。

 [https://www.youtube.com/embed/wb1hOdN888k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wb1hOdN888k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

