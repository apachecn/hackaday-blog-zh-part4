# TWANG32 为 ESP32 带来了 LED 条形游戏

> 原文：<https://hackaday.com/2022/05/05/twang32-brings-led-strip-gaming-to-the-esp32/>

在 Hackaday 电视下面是一个现代的游戏控制台，这是一个众所周知的模型，你们很多人可能也有，它的主要功能是一个 3D 加速器，允许它创建我们都知道并喜欢的美丽的渲染世界。[Mircemk]在 Twang 项目中避免了这些华而不实的东西，因为[这不是一个 3D 游戏，也不是 2D，而是 1D](https://hackaday.io/project/185011-twang-esp32-led-strip-1d-game) 。显示器，实际上是整个游戏表面，是一条可寻址的发光二极管，可以在休息时间下方的视频中看到。

在这一切的背后是一个 ESP32，以及一个使用加速度计的独特的一维操纵杆。还有一个带小压电扬声器的音频通道，LED 灯条是 DFRobot 的一种特别高密度的灯条。因为这是一个 ESP32 驱动的设备，它有 WiFi，在其上暴露了网络的接入点，通过该接入点以网页的形式提供游戏统计数据。它可能不会取代现代游戏机，但它确实很有创意。

长期的黑客读者会意识到，这只是一长串一维游戏中的最新一款，其中包括由 T2 和 1D 挑战著名的乒乓游戏。

 [https://www.youtube.com/embed/_6ZrDjNiuQI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_6ZrDjNiuQI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

