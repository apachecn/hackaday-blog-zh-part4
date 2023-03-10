# 加速对 MCU 连接的串行显示器的绘制

> 原文：<https://hackaday.com/2019/09/23/speeding-up-drawing-to-mcu-connected-serial-displays/>

得益于 MIPI 联盟定义的标准，如今从微控制器向串行连接(SPI/I2C)显示器写入图像数据非常容易，但其中也有一些陷阱，可能会让使用它的人措手不及。[【Larry Bank】写了一篇很好的总结](https://bitbanksoftware.blogspot.com/2019/08/optimizing-access-to-serial-i2cspi.html)，讲述了如何从这种显示链接中获得最佳性能。

核心是像素数据和命令传输之间的区别。从命令模式变为像素数据模式需要信令，这占用了 MCU 和显示器之间传输像素数据的宝贵时钟周期。通用的 [MIPI DCS 指令集](https://www.mipi.org/specifications/display-command-set)允许寻址部分显示器，而不是要求完全刷新，从而大大减少了所需的数据传输。然而，如果不对命令和数据传输进行适当的分段，最终会不必要地减慢处理速度。

结果是，我们可以在 AVR MCU 上运行类似 Pac-Man 仿真器的东西，AVR MCU 配有速度为 60 FPS 的 320×480 SPI LCD，正如我们在休息后嵌入的视频中看到的那样。查看文章中的另一个演示视频。

 [https://www.youtube.com/embed/DCkTWyz7Syo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DCkTWyz7Syo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



(感谢[nebk]发送此消息)