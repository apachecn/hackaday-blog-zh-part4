# 微控制器上的 Micropython

> 原文：<https://hackaday.com/2020/11/14/micropython-on-microcontrollers/>

有许多小型微控制器可用于各种任务，每一个都有其独特的特性和功能。然而，并不是所有人都想花时间在 C 或汇编语言上瞎折腾，来学习每个不同芯片的复杂性。如果你更喜欢 Python 的更高层次，由于 MicroPython，[(Rob)在这个基于 ESP32](https://robdobson.com/2020/11/embedding-micropython-on-esp32/) 的项目中向我们展示了 MicroPython，即使是最小的微控制器也不是不可能的。

[Rob]一直在研究一个名为 Marty 的小型机器人，它使用 ESP32 作为其大脑，因此小型微控制器已经承担了 WiFi/蓝牙通信和驱动机器人电机的任务。让 Python 在这样的平台上运行的部分问题是，MicroPython 被设计为在任何时候都是唯一在设备上运行的东西，但由于 ESP32 比 MicroPython 的最低要求更强大，他想看看他是否可以运行更多的 Python 代码。他最终决定采用“自下而上”的方法为平台构建一个库，而不是直接将 MicroPython 作为 ESP32 的固件映像来实现。

这篇博文有趣地介绍了在小型平台上运行 Python 代码的情况，并详细介绍了[Rob]最终为这个项目解决的 MicroPython 本身的缺点。他还在自己的 GitHub 页面上发布了自己作品的源代码。当然，对于在同一个小型处理器上运行 Python 和 C 的不同方法，[有一些库也可以完成这个任务](https://hackaday.com/2019/08/31/micropython-and-c-play-together-better/)。