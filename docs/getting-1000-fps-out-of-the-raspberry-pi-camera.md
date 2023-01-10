# 从 Raspberry Pi 相机获得 1000 FPS

> 原文：<https://hackaday.com/2020/03/11/getting-1000-fps-out-of-the-raspberry-pi-camera/>

Raspberry Pi 摄像头已经成为许多创客项目事实上的标准，使对象识别和远程流媒体等事情变得轻而易举。然而，所使用的索尼 IMX219 相机模块能够做得更多，并且[Gaurav Singh]开始释放它的能力。

研究 IMX219 数据手册后，很明显，当配置为使用其全部四个 MIPI CSI 通道时，它可以在更高的带宽[下工作。在 Raspberry Pi 模块中，只使用了两条 MIPI 通道，限制了相机的帧率。相反，[Gaurav]开发了一个定制的 IMX219 分线模块，允许摄像机使用所有四个通道连接到 FPGA，以实现更大的吞吐量。](https://www.circuitvalley.com/2020/02/diy-imx219-4-lane-mipi-breakout-board-raspberry-pi-camera-fpga-4-lane-mipi-csi.html)

[有了这个功能，就有可能以高达 1,000 fps 的帧速率使用摄像机](https://www.circuitvalley.com/2020/02/imx219-camera-mipi-csi-receiver-fpga-lattice-raspberry-pi-camera.html)。这是通过将 IMX219 直接连接到 FPGA，然后连接到主机的 USB 3.0 接口来实现的，而不是使用原始的 Raspberry Pi 接口。虽然 1，000 fps 仅在 640 x 80 的低分辨率下可用，但在 1080p 下也可以以 60 fps 拍摄，甚至在 3280 x 2464 下可以以 15 fps 拍摄。

虽然这可能超出了普通用户所需的性能范围，但[Gaurav]很好地证明了，如果您真的需要，桌面上通常还有一些功能。Github 上为那些渴望深入研究的人提供了资源。我们已经看到其他人也使用先进的技术来[提高 IMX219 的帧速率。](https://hackaday.com/2019/08/10/660-fps-raspberry-pi-video-captures-the-moment-in-extreme-slo-mo/)休息后的视频。

 [https://www.youtube.com/embed/uRaHXo-Zu90?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uRaHXo-Zu90?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

