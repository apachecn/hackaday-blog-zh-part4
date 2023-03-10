# 计算机视觉可以让你看一眼就跳过歌曲

> 原文：<https://hackaday.com/2021/11/02/computer-vision-lets-you-skip-songs-with-a-glance/>

你有没有希望你可以控制你的家庭自动化设备，除了一个枯萎的凝视？那么你很幸运，因为[【诺伯特·扎雷亚】想出了一个只用你的脸控制 MP3 播放器的聪明方法](https://hackaday.io/project/182328-skip-songs-just-with-looking)。虽然正如你可能想象的那样，这项技术可以通过一些小的调整应用于整个范围的家庭自动化任务。

这个项目的核心是 Raspberry Pi，特别是 3 B+模型，尽管随着计算机视觉的计算需求，您可能希望将其提升到最新最棒的 Pi 4。从那里你需要加载 OpenCV 和一个为人脸检测训练的模型，幸运的是，这是这项技术的一个相当常见的应用。

[![](img/fd07cf8abaaa2b8c0ac2447c0c64b017.png)](https://hackaday.com/wp-content/uploads/2021/10/faceskip_detail.jpg) 通过一个相对简单的 Python 脚本，[Norbert]能够确定 OpenCV 何时检测到他正直视相机，并触发 Pi 的一个 GPIO 引脚，该引脚已连接到物理 MP3 播放器上的“跳过”按钮。没错，你没看错。他在 2021 年使用专用的 MP3 播放器。

说真的，我们真的不知道为什么[Norbert]走这条路，而不是简单地在 Pi 上播放音乐并通过软件控制它，但这确实是一个很好的例子，说明如果需要，你可以如何与物理设备进行交互。在任何情况下，使用他提供的 Python 脚本，您都可以轻松地修改设置来控制其他任务，无论是虚拟的还是其他的。

[虽然人脸识别在野外可能是一件可怕的事情](https://hackaday.com/2019/01/02/your-face-is-going-places-you-may-not-like/)，但我们确实认为它在家庭中有一些有趣的应用，只要用户是控制他们数据最终去向的人。

 [https://www.youtube.com/embed/ojnZvVBBWRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ojnZvVBBWRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

