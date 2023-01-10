# ESP32-Cam 是一款出色的运动检测器

> 原文：<https://hackaday.com/2021/10/23/esp32-cam-makes-a-dandy-motion-detector/>

万圣节就要到了，几乎每个万圣节项目都需要某种运动传感器。历史上，我们一直使用红外和超声波传感器，但[Makers Mashup]决定在他最新的电子动画创作中使用 ESP32-Cam 作为运动传感器。你可以在下面看到该设备的视频及其工作原理。

这个项目是一个头骨，通过步进电机的几度运动跟随你。有一个 [3D 打印的](https://www.thingiverse.com/thing:5027173)外壳，使硬件组装变得容易。基础软件是从【口才 Arduino】借来的。

算法非常简单。该代码抓取一帧视频，并将其分成 10 个垂直区域，每个区域代表步进电机的每一度运动。它用 10 列中的每一列的值创建一个数组。通过这种方式，代码可以检测一个区域的变化，并跟踪该运动。

除了头骨，还可以看到摄像机驱动着一个巨大的充气眼球。虽然红外或超声波测距仪的作用范围不大，但眼球可以很容易地跟踪远处人行道上的人，只要他们在画面中。坏处呢？你确实需要场景被照亮。为了解决这个问题，有一个 30 美元的红外线泛光灯可以解决这个问题。谁想要一个灯火通明的万圣节项目？

无论如何，如果你必须在你的设备上安装一个摄像头，这种技术是显而易见的。即使你不需要相机，价格足够低，你也可以获得一些有趣的好处，如增加的范围。

如果你想在轮子上安装一个 ESP32-Cam，[看看这个机器人](https://hackaday.com/2020/02/19/lil-esp32-bot-does-remote-surveillance-and-its-easy/)。现在有了一个现成的[编程板](https://hackaday.com/2020/01/09/add-on-board-makes-esp32-camera-board-easier-to-program/)，这些设备甚至更容易使用。

 [https://www.youtube.com/embed/NIbiG6at01g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NIbiG6at01g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

