# ESP32 频谱分析仪接入两个内核

> 原文：<https://hackaday.com/2020/12/10/esp32-spectrum-analyzer-taps-into-both-cores/>

我们可能不需要告诉普通黑客读者，ESP32 是一款功能强大、极其灵活的微控制器。在过去的几年里，我们已经看到了一些令人难以置信的项目使用这种价格合理的芯片，从表面上看，最好的还在后面。这是因为在社区真正明白如何最大限度地利用硬件之前，总是需要一些时间。

以[squix]最近在研发的蓝牙音频播放器为例。使用 esp32-a2dp 库播放音乐没有问题，但当他想要添加一些可视化效果时，音频质量受到了严重影响。意识到他的快速傅立叶变换(FFT)代码消耗了太多的处理器能力，这似乎是他探索使用 ESP32 第二内核的大好时机。

[squix]过去一直避免探究 ESP32 的双核特性，认为第二个内核正忙于处理 WiFi 通信。但通过使用 FreeRTOS 队列系统，他编写了一些代码，用一个内核收集音频数据，并在另一个内核上运行实际的 FFT 魔术。通过像这样平衡工作负载，他能够在休息后驱动视频中看到的 Icon64 前面的 64 个 WS2812B LEDs 阵列。

即使你对运行自己的微控制器 disco 不太感兴趣，这个项目可能就是你一直在等待的例子，帮助你在 ESP32 上处理多任务。如果你想[掌握一个有这么多锦囊妙计的设备](https://hackaday.com/2018/02/22/software-defined-television-on-an-esp32/)，你将需要所有你能得到的帮助。

 [https://www.youtube.com/embed/1UpbtE98OBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1UpbtE98OBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

