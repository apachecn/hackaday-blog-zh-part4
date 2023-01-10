# 一个 LED 立方体显示中央处理器的生命

> 原文：<https://hackaday.com/2020/10/04/an-led-cube-to-display-cpu-vitals/>

LED 立方体现在风靡一时。能够驱动大型阵列的高端硬件价格越来越便宜，3D 打印机和预制电路板可以使组装变得轻而易举。在参加了一个大型黑客大会并看到了展出的版本后，[Sebastian]想要分一杯羹，于是开始建造自己的版本。

虽然许多人选择建造一个可以拿在手中的 LED 立方体，但[Sebastian]更喜欢固定的桌面设计。这将降低成本，允许他只使用 3 个 LED 板，因为底座和剩余的两个侧面将背对着他，当放在他的桌子上时不可见。64×64 阵列由树莓 Pi 2 顶部的 Adafruit LED 矩阵罩驱动。Pi 是一个战术选择，因为[Sebastian]身边就有一个，它有足够的处理能力来运行 OpenGL 着色器，该着色器为立方体创建图像，该图像随主桌面上的 CPU 负载和温度而变化。作为最后一点，Raspberry Pi 设置了一个只读文件系统。这允许项目被突然关闭，而没有损坏 SD 卡的风险。

这是一个整洁的建筑，给[塞巴斯蒂安]有用的信息一目了然。[我们以前展示过一些时尚的立方体、](https://hackaday.com/2019/09/05/handmade-led-cube-is-a-work-of-art/)和[，甚至还有一款 LED D20，它真的让我们倾家荡产。](https://hackaday.com/2020/09/16/the-most-expensive-d20-youll-see-today/)休息后的视频。

 [https://www.youtube.com/embed/QqknzoxHMFo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QqknzoxHMFo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

