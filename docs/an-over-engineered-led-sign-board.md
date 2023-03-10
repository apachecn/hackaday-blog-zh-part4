# 一个过度设计的 LED 标志牌

> 原文：<https://hackaday.com/2018/12/08/an-over-engineered-led-sign-board/>

永远不要低估制造者在过度思考和过度设计最简单的问题以及展示人类创造力方面的能力。特隆赫姆[Hackheim hackerspace]的[Hans 和他的团队]制作的 RGB LED 标牌就是这一事实的证明。

正如您所料，WS2812 RGB LEDs 照亮了标志。在这种特殊的结构中，一个单独的条负责每个字符。该标志由运行 FreeRTOS 的 ESP32 驱动，使用 MQTT 进行通信，每个字母都获得一个 6 x 20 帧缓冲区的副本，该缓冲区代表预期显示的颜色模式。ESP32 上的任务计算每个 LED 要显示的颜色值。

真正的问题是，如何校准分布的发光二极管串，使标志相邻字母上的发光二极管显示外推值？答案是使用 OpenCV 创建 led 从二维布局到查找表的映射。Python 脚本发送命令点亮单个 LED，用 OpenCV 捕获的图像记录信号的位置。对所有 led 重复这一过程，以生成在 ESP32 固件中使用的映射。多酷啊。

如果你对代码有疑问，它在[ [Github](https://github.com/hansihe/led_sign) ]上，我们很乐意看到有人把它提升一个层次。校准代码，以及远程客户端和 ESP32 代码，都是为您的黑客乐趣。

我们已经有一段时间没有看到 OpenCV 像[运动跟踪转台](https://hackaday.com/2017/08/04/opencv-turret-tracks-motion-busts-airsoft-pellets/)和[人脸识别](https://hackaday.com/2017/12/11/opencv-never-forgets-a-face/)那样工作了。可能性似乎是无限的。

[https://gfycat.com/ifr/dismalglossyduckbillplatypus](https://gfycat.com/ifr/dismalglossyduckbillplatypus)