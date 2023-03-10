# Arduino 钻机做分光光度法

> 原文：<https://hackaday.com/2020/08/24/arduino-rig-does-spectrophotometry/>

分光光度法是一种重要的科学工具，最常用于生物学和化学。这是一种测量化学溶液在不同波长下吸收的光量的方法。虽然这通常是昂贵的实验室设备的专用品，但[丹尼尔·辛斯顿]建造了一个钻机在家里做这项工作。

该装置的核心是一个普通的灯丝手电筒灯泡，它能产生包含所有颜色的优质白光。然后用棱镜将光分成不同的波长，这样就可以在整个光谱范围内测试样品。棱镜由伺服电机旋转，使样品暴露在完整的彩虹下，而 Arduino 使用光敏电阻来测量有多少光穿过样品。因此，相对于没有样品存在时进行的校准，可以计算样品吸收的光量。

这是一个简单的构建，可以用相当普通的材料实现，除了可能需要特别定制的棱镜。这将是向高中生传授先进科学概念的好方法，也是向他们展示实验室设备如何工作的好方法。

我们在这里看到各种各样的 DIY 科学装备；这个基于灯笼的生物反应器就是一个很好的例子。休息后的视频。

 [https://www.youtube.com/embed/vP9oaMI_R7s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vP9oaMI_R7s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

