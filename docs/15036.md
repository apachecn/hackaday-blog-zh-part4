# 鱼儿喂得饱饱的，睡得安稳

> 原文：<https://hackaday.com/2022/10/10/sleep-easy-with-the-fishes-well-fed/>

有时候日常任务，比如喂养宠物，会感觉像是一件很麻烦的事情。为了帮助缓解日常生活中的世俗问题，[埃里克·贝里隆德]创造了一个[自动喂鱼器](https://www.thingiverse.com/thing:5517562)，配有 3D 打印文件、固件和一个 Android 应用程序，可以完全控制时间安排和喂食。

喂鱼器的机械结构包括一个螺旋输送系统，该系统推动从食物储存盆喂入的食物颗粒。螺旋输送机由 Feetech FS5106R 伺服系统驱动，该伺服系统提供足够的力来克服颗粒卡在输送机系统中可能发生的堵塞。[埃里克·贝里隆德]写道，该系统每秒可以分配大约 0.9 克，它是为颗粒状食品设计的，因为薄片有问题，因为“它们的低密度和大表面积容易使它们卡在料斗的喉部”——这个问题[我们以前已经研究过](https://hackaday.com/2022/05/24/handling-bulk-material-why-does-my-catfood-get-stuck/)。

[埃里克·贝里隆德]使用[科伯达斯]的[喂鱼器](https://www.thingiverse.com/thing:301532)作为基础，用更好的伺服系统升级它，添加一个树莓 Pi Zero W 以及 Pi 软件和一个 Android 应用程序来控制喂食时间表。还有一个 DS1307 实时时钟模块来保持精确的时间，还有一个按钮用于“手动”喂食。如果你想在家跟进，你可以在各自的 GitHub 库中找到运行在 Pi 上的 [Python 脚本和 Android 应用程序](https://github.com/erikjber/Fish-Feeder-Raspberry-Pico-W)的[源代码。](https://github.com/erikjber/Fish-Feeder-App)

 [https://www.youtube.com/embed/4nPhB9u4AYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4nPhB9u4AYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

