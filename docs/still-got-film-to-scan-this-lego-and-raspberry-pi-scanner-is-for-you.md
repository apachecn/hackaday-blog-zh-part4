# 还有胶片要扫描吗？这个乐高和树莓派扫描仪是给你的

> 原文：<https://hackaday.com/2020/12/11/still-got-film-to-scan-this-lego-and-raspberry-pi-scanner-is-for-you/>

在大众数码摄影的早期，胶片扫描仪是一种常见的景象。一个通常连接到 USB 端口的小盒子，它有一个用于幻灯片或底片的插槽。在 2020 年，它们是稀有品种，但不要害怕！[Bezineb5]有一个解决方案，形状是[一个使用 Radpberry Pi 的自动扫描仪和一个由 Lego 制成的机械装置](https://github.com/bezineb5/RoboScan)。

乐高机械装置是一个链轮进给器，将胶片从单反相机的视野中移动过去。Pi 上的软件运行在 Docker 容器中，并采用机器学习方法来确定帧边界。这超出了 Pi 的能力，所以被卸载到 Google Coral 加速器。

整个过程是自动化的，Pi 不仅控制乐高积木，还控制相机，从相机中检索照片到 Pi。有一个智能网络界面来控制一切，让这个过程——请原谅这个双关语——变得轻而易举。这是一个视频，你可以在画面下方看到。

这些年来，我们推出了许多电影扫描仪项目，其中一个令人难忘的是[这个 3D 打印镜头支架](https://hackaday.com/2018/02/19/scan-your-film-the-3d-printed-way/)。

 [https://www.youtube.com/embed/yRDomN48SOs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yRDomN48SOs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Via [r/raspberry_pi](https://www.reddit.com/r/raspberry_pi/comments/k9476e/roboscan_a_raspberry_pibased_automated_analog/) 。