# 一个开源的 HDMI 采集卡

> 原文：<https://hackaday.com/2022/10/14/an-open-source-hdmi-capture-card/>

[YuzukiHD]为任何希望在家中构建自己的 HDMI 采集卡的人提供了文件。这种设计被称为希礼环路输出 HDMI 采集卡 PRO，简称 YuzukiLOHCC PRO。

该版本基于 MS2130，这是一款与 USB 3.2 Gen 1 兼容的高清视频和音频捕获芯片。我们 [*非常确定*](https://hackaday.com/2022/04/03/is-your-device-actually-usb-3-0-or-is-the-connector-just-blue/) 现在被称为 USB 3.2 Gen 1×1，该标准能够以高达 5 Gbps 的速度传输。因此，该芯片可以支持高达 4K 分辨率、60 Hz 的 HDMI，具体取决于线路上传输的确切信号。它与 YUV422 & MJPEG 模式兼容，可以与 OBS Studio 和 FFmpeg 等软件一起使用。棋盘本身相对简单。它具有一个 HDMI 输入端口、一个 HDMI 输出端口和一个 USB-C 端口，用于连接到计算机进行捕捉。

HDMI 捕捉卡可能很贵，也很麻烦，所以你可能会发现自己动手做更划算。此外，在 V2 CERN 开放硬件许可证下开源意味着如果你愿意，你可以做出改变来适应你自己的用例。

这些年来，我们已经看到了一些其他搞笑的视频捕捉技巧，比如一个复杂的装置[,它使用 SNES 将游戏机摄像头变成可用的网络摄像头。](https://hackaday.com/2021/07/25/dominate-video-calls-with-game-boy-camera-webcam/)如果你的实验室正在酝酿任何这样的疯狂黑客，一定要[让我们知道！](https://hackaday.com/submit-a-tip)