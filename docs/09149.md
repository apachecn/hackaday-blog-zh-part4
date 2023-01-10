# Arducam 现在使用 RPi Pico

> 原文：<https://hackaday.com/2021/02/02/arducam-now-working-with-the-rpi-pico/>

树莓派 Pico 完全不知从哪里冒出来，并席卷了制造商世界。以 4 美元的低成本，包装一些真正的原始硅，甚至可以在杂志封面上免费获得，它已经拥有了一大批粉丝。与任何新的流行平台一样，人们争相让一切都在硬件上运行。ArduCAM 已经在 Raspberry Pi Pico 上运行了！

ArduCAM 基于 OV2640 图像传感器，内置 JPEG 编码器，非常适合微控制器应用。这就限制了微控制器处理来自摄像头的图像所需的 RAM 数量。随着 Pico 现已上市，ArduCAM 背后的团队开始编写一个库，以使所有东西都能与 SPI 摄像头完美配合。可以从 Github 上获得，并附有一个示例程序，这样你就可以开箱检查一切是否正常。启动和运行的最简单方法是从 Raspberry Pi 环境，但 Pico 充当 USB 大容量存储设备，因此几乎可以在任何地方进行编程。

在接下来的几个月里，我们很可能会看到整个系列的微控制器被移植到 Pico 上，同时还有许多特殊 IO 特性的有趣用途。休息后的视频。

 [https://www.youtube.com/embed/xekoG8cPvyE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xekoG8cPvyE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

