# 激光特雷门琴把你的手变成音乐

> 原文：<https://hackaday.com/2021/10/03/laser-theremin-turns-your-hand-swooshes-into-music/>

在一个智能手机已经商品化精密 MEMS 传感器的世界里，这一阶段将把这些传感器重新想象成完全不同的东西。这正是[chronopoulos]所做的，他采用了四个接近传感器，并将它们变成了一个定制的手势输入传感器，用于生成声音。结果是[象限](https://hackaday.io/project/165541-quadrant)，一个可重复使用的人机界面设备，被证明在检测手势并将其转化为音乐方面表现良好。

在其核心，象限是一个围绕 STM32F0 和四个 VL6180X 飞行时间接近传感器构建的人机界面设备。这个想法是从设备端尽可能快地传输测量的距离数据，然后在 PC 端将其转换为音乐交互。不过，计算距离需要一些时间，所以[chronopoulos]对数组进行流水线读取，通过 USB 以相当高的 30 Hz 将数据传输到 PC。

有了在 PC 端收集的数据，就有可能进行广泛的互动。想要激光竖琴吗？没问题，因为[chronopoulos]展示了如何“拨动”虚拟弦。方位传感器怎么样？只需将手伸到阵列上，改变角度。最后，四个传感器还可以让你检测阵列上掠过的手势，比如你的手从一边到另一边的嗖嗖声。为了了解这些互动，请在休息后的 [2:15 分](https://youtu.be/oI8qlKoX1z4?t=135)跳转到视频演示。

如果你想深入了解这个项目的内部运作，[chronopoulos]已经友好地将[固件](https://github.com/chronopoulos/quadrant-firmware)、[原理图和布局文件](https://github.com/chronopoulos/quadrant-board)放在 Github 上，并获得了慷慨的麻省理工学院许可。他甚至发布了一篇配套论文[[PDF](https://cdn.hackaday.io/files/1655417082506144/quadrant_nime2019.pdf)，详细介绍了检测这些手势背后的数学原理。最后，如果你只是想切入正题，创作自己的音乐，你也可以在 Tindie 上找到这首歌。

如今，MEMs 传感器在我们的手机之外正过着美好的第二人生，这个项目再次证明了它们为新项目创意提供的丰富性。对于更多基于 MEMs 传感器的项目，看看这个[自平衡机器人](https://hackaday.com/2019/06/14/augmented-arthropod-gets-a-self-balancing-ride/)和[魔杖](https://hackaday.com/2018/12/07/magic-wand-learns-spells-through-machine-learning-and-an-imu/)。

 [https://www.youtube.com/embed/oI8qlKoX1z4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=52&wmode=transparent](https://www.youtube.com/embed/oI8qlKoX1z4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=52&wmode=transparent)

