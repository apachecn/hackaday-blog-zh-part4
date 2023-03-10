# 一个不停转动的翻转钟

> 原文：<https://hackaday.com/2022/10/13/a-flipping-perpetually-rotating-clock/>

时钟是黑客和制造商的支柱，因为它们提供了一种探索创造性设计的方式，同时还保持了项目的功能性。[Brett Oliver]遵循这一传统，制作了一款[回旋时钟](http://www.brettoliver.org.uk/Cyclotron_Clock/Cyclotron_Clock.htm?i=2)，它使用了 20 世纪桌面翻转日历中的永久旋转数字概念。

![An exploded view of one of the flip calendar digit display, showing how the tiles fit into the chamber.](img/07ff4c8f8fdce17834201394773d60b3.png)

时钟的每个数字都有一个足够大的旋转室，可以容纳一组两面都印有数字的瓷砖。瓷砖的尺寸和堆叠方式应确保旋转室可以让下一个瓷砖在旧瓷砖的前面滑动。通过旋转腔室若干次来显示特定的数字。

四个数字位置中的每一个都有一个 28BYJ-48 步进电机来旋转室，每个电机都由 ULN2003 驱动模块驱动。主微控制器是一个 ESP32 WROOM，与 I2C 兼容的 DS3231 实时时钟(RTC)模块保持时间。所有电机都由提供 7 V 电压的 LM2596 模块驱动，而 ESP32 和 RTC 由 USB 连接器供电。

不同的模式和设置时间的能力是通过一个有各种按钮和旋钮的面板来完成的。整个时钟安装在一个定制的木制底座上，底座上有用于面板和电缆的切口。[Brett Oliver]在文档方面做得很好，详细介绍了建筑的机械和电子设备。设计文件，包括各种组件的 STL，也可以下载。休息后请务必观看视频。

我们推出了一款[翻转日历](https://hackaday.com/2018/03/23/diy-perpetual-flip-calendar/)，其操作原理与之前类似，可以清楚地显示机械装置的内部工作原理。

 [https://www.youtube.com/embed/MCAMvnq7D7I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MCAMvnq7D7I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

