# 使用 ESP32 VGA 显示器返回视频基础知识

> 原文：<https://hackaday.com/2019/02/05/back-to-video-basics-with-an-esp32-vga-display/>

在一个标准以惊人的速度来来去去的世界里，VGA 有些令人欣慰的地方。这是视频标准的最小公分母，在电脑背面看到那个矮胖的 DB15 连接器意味着无论如何，你都可以从中获得一些东西，如果你能在垃圾箱中找到一根 VGA 电缆的话。

但那是个人电脑的世界；微控制器呢？能哄他们 VGA 视频吗？[是的，你可以](http://bitluni.net/esp32-vga/)，用一个 ESP32，一些电阻，和一点点巧妙的编程。至少这是[bitluni]在继续推动 ESP32 输出所有信号的过程中成功做到的。在这个项目中，[bitluni]需要产生三个独立的信号——红色、绿色和蓝色——但只有两个 DAC，他不得不尝试其他方法。他用 R/2R 分压器网络的老方法构建外部 DAC，并在 LCD 模式下通过 I2S 总线寻址。他需要做出一些妥协，以将三种颜色信号以及水平和垂直同步脉冲放入 24 个可用位中，并且有一些错误的开始，但下面的视频显示他能够产生 320×240 信号，并最终将其提升至非原生的 460×480。

这是一个非常令人印象深刻的技术，通过观看视频，我们了解了很多关于 ESP32 和 VGA 标准的知识。他之前用 ESP32 建造了一个调幅广播电台(T1)，并让 T2 输出复合 PAL 视频(T3)，甚至 T4 用它把他的示波器变成了矢量显示器(T5)。它们都是很好的学习项目。

 [https://www.youtube.com/embed/G70CZLPjsXU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G70CZLPjsXU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[anacierdem]为我们挑选了这个。