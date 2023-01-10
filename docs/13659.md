# 运行在微型微控制器上的 OpenCV

> 原文：<https://hackaday.com/2022/05/19/opencv-running-on-tiny-microcontroller/>

乍一看，大量使用计算机视觉或机器学习的项目似乎需要基于强大的计算平台，这些平台具有足够的时钟周期和内存来处理这种类型的应用。虽然这有一定的道理，但随着该领域的发展，也有可能在低功耗设备上试验这些工具。[以这个完全基于 ESP32 构建的 OpenCV 项目为例](https://www.youtube.com/watch?v=7qPIRBY6C8c)。

也就是说，为了以任何有意义的方式使用 OpenCV，需要对 ESP32 进行一些修改。其中最重要的是 ESP32-DOWDQ6 模块的使用，该模块增加了 ESP32 的可用内存，使其能够更好地利用相机功能。即使这样，ESP32 也不能运行整个 OpenCV 应用程序，因此在设备可以本机运行 OpenCV 之前，需要一个精简版的 OpenCV。然而，一旦这两个障碍被排除，像边缘检测这样的事情，正如这个项目所展示的，就完全有可能实现。

如果 OpenCV 可以在像 ESP32 那么小的东西上运行，那么在功能更强大但仍然便宜的东西上运行就更容易了，比如 Raspberry Pi。虽然这个项目的代码可以在 GitHub 页面上找到，但我们在更强大的平台上也有很多其他 OpenCV 项目，比如[这个时钟，每当有人看到它就会从墙上掉下来](https://hackaday.com/2021/09/14/useless-machine-is-a-clock/)。

 [https://www.youtube.com/embed/7qPIRBY6C8c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7qPIRBY6C8c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[ninjan33r]的提示！