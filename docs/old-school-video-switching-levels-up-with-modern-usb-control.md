# 老式视频切换水平与现代 USB 控制

> 原文：<https://hackaday.com/2022/12/10/old-school-video-switching-levels-up-with-modern-usb-control/>

如今，视频效果和混音都是数字化的，但并非一直如此。当模拟技术统治视频世界的时候，一个大的开关面板是有效结果的关键。

[![](img/d39f08587fee19731e8699bd431fb1fa.png)](https://hackaday.com/wp-content/uploads/2022/12/vlcsnap.png)

VIdeo like this was the result of combining different analog feeds with different effects. The better the hardware, the more was possible.

像[Glen]的[Grass Valley 系列 300 交叉点开关面板](https://bikerglen.com/blog/grass-valley-300-crosspoint-multiplexing/)这样的设备是那个世界的重要组成部分。有了这样的工具，操作人员可以建立真正的[所见即所得](https://en.wikipedia.org/wiki/WYSIWYG)风格的合成预览提要，并根据提示切换到直播。所有这些都是用相对简单的 CMOS ICs 和按钮完成的。很多很多按钮。

[Glen]逆向设计面板以展示其工作原理，大部分繁重工作由 MC14051B 模拟多路复用器/解复用器和 MC14532B 8 位优先级编码器完成。一旦想通了这一点，就可以通过使用微控制器来驱动设备，将它变成 USB 外设，从而实现一些现代化。

通过一点设计工作，[Glen]围绕 EFM8UB2 8 位微控制器构建了一个 PCB，作为 USB 外设并控制开关面板，负责按键扫描和灯控制等工作。最后一步:通过 USB 监控面板的 GUI 应用程序。

这不是[Glen]第一次与老式视频混合和切换接口，正如我们许多人所知，有时与现有硬件接口是一项棘手的工作。我们报道了他早期的视频切换器项目，使用的硬件远没有这个那么容易操作。