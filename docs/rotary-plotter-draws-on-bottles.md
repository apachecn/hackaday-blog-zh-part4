# 旋转绘图仪在瓶子上绘图

> 原文：<https://hackaday.com/2020/11/11/rotary-plotter-draws-on-bottles/>

笔式绘图仪通常是许多雄心勃勃的制造商对计算机数字控制(CNC)世界的第一次体验。虽然它们通常在平面上操作，但如果构造合适，它们也可以设计成在曲面上绘图—[正如[tuenhidy]用这款旋转式瓶子绘图仪展示的那样。](https://www.instructables.com/ROTARY-CNC-BOTTLE-PLOTTER/)

绘图仪使用从一台旧打印机中回收的轴作为瓶子的滚筒，由一对步进电机驱动。x 轴和 Z 轴是由两个 CD 驱动机构创建的—[这是一种廉价构建两个线性轴的流行方式。](https://hackaday.com/2019/04/29/build-a-plotter-using-scrap-dvd-drives/)硬件由 GRBL 控制，运行在 Arduino Uno 上，配备了 CNC 保护罩来处理必要的 I/O。

构建在某种程度上受限于其 X 轴的短范围，这使得绘图仪无法轻松地在全尺寸的瓶子标签或罐子上绘图。然而，如果需要的话，这可以通过一些升级和额外的步进器很容易地解决。作为一个家庭建筑，这是一个很好的方式来学习数控技术所需的工作曲面有效。休息后的视频。

 [https://www.youtube.com/embed/rRHOq8oxpGU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rRHOq8oxpGU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

