# 使用 PIR 和 Arduino 避免尴尬的视频会议情况

> 原文：<https://hackaday.com/2021/07/24/avoid-awkward-video-conference-situations-with-pir-and-arduino/>

定期在家开视频会议有其挑战性，尤其是如果你有孩子的话。为了避免尴尬的局面，[Charitha Jayaweera]创造了[Present！](https://hackaday.io/project/180761-present-availability-sensing-for-zoom-meetings)，一个 USB 设备，如果你突然需要离开你的*电脑*来维持家庭秩序，它会自动关闭你的相机和麦克风。

Present 仅由一个 PIR 传感器和 Arduino 组成，位于一个 3D 打印外壳中，可安装在您的显示器上。当 PIR 传感器不再检测到范围内有人时，它会通过串行向 PC 上运行的 python 脚本发送通知，以关闭 Zoom(或另一个应用程序)上的摄像头和麦克风。当你再次坐下时，它可以选择性地打开这些开关。廉价的 HC-SR501 PIR 模块的范围也可以根据您的具体情况使用 trimpot 进行调整。使用小型定制 PCB 或众多兼容 Arduino 的小型开发板之一，也可以将器件缩小到 PIR 模块的尺寸。

要快速手动静音，请查看[巨型 3D 打印静音按钮](https://hackaday.com/2021/07/20/one-giant-button-to-mute-them-all/)。礼物是一张参加[在家工作](https://hackaday.com/2021/07/16/final-weekend-for-work-from-home-challenge-of-the-hackaday-prize/)挑战赛的入场券，这是 [2021 黑客日奖](https://prize.supplyframe.com/)的一部分。

[hack adayprize 2021](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)