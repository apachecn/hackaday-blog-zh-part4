# 通过鼠标传输视频

> 原文：<https://hackaday.com/2021/07/30/streaming-video-from-a-mouse/>

第一个光学鼠标必须在一个特殊印刷的鼠标垫上使用，鼠标垫上有印刷网格，四象限红外传感器可以检测到。后来，小鼠将红外传感器换成了光电模块(本质上是一种微小的、分辨率非常低的相机)和强大的图像处理功能。有一天，当他们决定破解游戏鼠标中的固件，并最终开始从内部的摄像头中传输[帧时，他们正躺在床上。](https://8051enthusiast.github.io/2020/04/14/003-Stream_Video_From_Mouse.html)

第一步是[分析鼠标和主机](https://8051enthusiast.github.io/2020/04/14/001-USB_Firmware.html)之间的协议。启动一个 Windows VM 和 Wireshark 允许他捕获所有到 USB 控制器的控制转移。因为它是一个“可编程”游戏鼠标，允许用户设置宏，所以[8051enthusiast]可以使用控制传输，该控制传输通常会查询已设置的宏，以返回任意位置的内存。经过一点点修补，他现在有了一个固件转储。查看最丰富的字节，它似乎符合类似于英特尔 8051 的配置文件。在逆向工程的迷人模糊中，他从为滚轮设置 LED 颜色的函数追溯到程序的主要结构(这取决于当前的 DPI 设置)。不幸的是，固件阻止了相同的宏机制写入任意位置。

浏览代码，一个很好的旧缓冲区溢出漏洞似乎是可能的，但它导致系统通过看门狗复位。所以他采取了另一种方法，调用恢复模式并在设备上加载全新的固件，这是一个`set_repor` t 控制转移可以调用的。

接下来，[他移动到 ADNS-9800 光学传感器](https://8051enthusiast.github.io/2020/04/14/002-Sensor_Firmware.html)(图片在由[杰克企业](https://www.tindie.com/stores/jkicklighter/)提供的顶部图像中)，它在固件中有一个大的加密斑点。一些打探和推断导致猜测光学传感器是另一个 8051 系统。凭借一些巧妙的推理和十足的决心，[8051enthusiast]能够用一个程序破解 XOR 流密码加密，该程序向他展示了多个版本的已拆卸程序集，并允许他选择最有可能的一个。随着固件的解密，他能够看到加密代码，并确认他推导出的算法。

 <https://hackaday.com/wp-content/uploads/2021/07/8051enthusiast_sensor-decrypt-1.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2021/07/8051enthusiast_sensor-decrypt-1.mp4](https://hackaday.com/wp-content/uploads/2021/07/8051enthusiast_sensor-decrypt-1.mp4)

随着传感器现在被打开，它进入了 30 x 30 240 fps 的视频流。传感器通过 SPI 进行通信，而 USB 控制器必须对连接进行位爆炸，因为它没有硬件。将两个定制的固件映像加上一些额外的功能是很容易的，但是 7 fps 就有些欠缺了。第一个优化是循环展开和移除固件中的一些休眠，这使它达到了 34 fps。通过测量单个指令的周期计数，他能够找到一些替代方案，如 mov 而不是少花一个周期的`setb`。从 17 个循环的循环到 11 个循环的循环和一些其他的优化给了他 54 fps。他并不满足于此，他修改了 ADNS-9800 固件，以连续采样，而不是等待 USB 控制器完成处理。虽然这产生了 100 fps，但还有更多工作要做:图像压缩。在高达 230 fps 的速度下，[8051 热情者]决定就此结束。

然而，他还想做最后一件事:用视频流控制鼠标。在他的基于 Python 的接收图像文件的程序中编写一些图像处理，让他可以使用鼠标，尽管这并不实际。

总而言之，这是[8051enthusiast]的一次不可思议的旅程，我们强烈建议您亲自阅读整个旅程。这不是他第一次修改基于 8051 的设备的固件，比如[修改他笔记本电脑](https://hackaday.com/2021/07/20/extracting-the-wifi-firmware-and-putting-back-a-keylogger/)中 WiFi 芯片组的固件。

【感谢 [JACK Enterprises](https://www.tindie.com/stores/jkicklighter/) 在 Tindie 使用[adns 9000](https://www.tindie.com/products/jkicklighter/adns-9800-laser-motion-sensor/)的形象】。