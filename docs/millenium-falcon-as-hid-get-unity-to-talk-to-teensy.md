# 千年隼隐藏:让统一与 Teensy 交谈

> 原文：<https://hackaday.com/2019/08/15/millenium-falcon-as-hid-get-unity-to-talk-to-teensy/>

这里有一个例子证明了一个硬件项目可以超越闪烁的 led 灯和将大量数据转储到串行控制台上。这些做法对某些人来说没什么问题，但[dimtass]已经找到了一个更文明时代的更优雅的方法。他的 3D 千年隼模型从他的 IMU 获得[方位数据，作为一个 HID 设备。](https://www.stupid-projects.com/controlling-a-3d-object-in-unity3d-with-teensy-and-mpu-6050/)

所涉及的硬件是一个 MPU6050 6 轴传感器，它与一个 Teensy 3.2 板接口。[dimtass]记录了他的校准 IMU 的方法，通过使用 Python 脚本来产生偏移。我们在过去提倡使用 Jupyter 笔记本，这是 Jupyter 在第二遍中绘制数据和可视化偏移效果的一个很好的例子。

运行时，Teensy 读取 IMU 数据，并通过 USB 原始 HID 接口发送。对于外行来说，HID 传输比 USB CDC 传输(虚拟串行端口)更可靠，因为它们在每个事件/事务中使用更小的数据块，并且通常不需要特殊的驱动程序 。 在计算机方面，【dimtass】编写了一个小应用程序，通过原始 HID 获取 IMU 值，然后提供给可视化应用程序。

在流行的开源游戏开发引擎 Unity 中渲染 3D 千年隼模型。尽管 Unity 有一个 API，但这种特殊的方法更多的是使用共享内存技术的操作系统特有的。HID 应用程序写入一个文件(/tmp/hid-shared-buffer)，然后 Unity 读取该文件，对渲染模型进行方向更改。

【dim tass】提供了许多关于将他的项目变为现实所使用的工具的细节，它可以成为更多需要将传感器与可视化系统连接起来的项目的良好开端。我们已经看到了把一个人的头变成操纵杆的方法，如果你需要[更深入地了解 Unity，不用再找了](https://hackaday.com/2017/06/21/youre-the-only-one-not-playing-with-unity/)。

 [https://www.youtube.com/embed/7xfACCh6LQw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7xfACCh6LQw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

