# LED 音乐可视化设备布满您的卧室

> 原文：<https://hackaday.com/2019/07/03/led-music-visualizer-bespeckles-your-bedroom/>

当谈到壁挂装饰时，准备扔掉你的小地毯，换上一件如此生动的东西，你会想要检查一下你的眼睛。为了让我们的眼睛暖和起来，詹姆斯·贝斯特发明了一个巨大的 900-RGB LED 音乐可视化器，确保我们的卧室根据需要变得明亮和闪亮。

像南加州那所小型文科学校的其他毕业生一样，[詹姆斯]开始用一些老式的蓝色胶带制作原型。一旦他确定了网格间距，他就开始用一些胶合板和木材制作 2 米乘 0.5 米的壁挂式显示器。在一些小的粘合事故之后，詹姆斯用胶带把他的网格钉了下来，准备好了视觉效果。

在引擎盖下，Teensy 正在利用其 DMA 功能向 900 个 led 传输比特流。通过使用 DMA 功能并选择使用 Arduino，James 正在使用空闲的 CPU 周期来制作一些傅立叶变换的音乐样本并显示它们的频率内容。

我们已经介绍了如何证明通过 DMA 驱动大量 WS2812B LEDs 的概念；很高兴看到这些想法成熟为一个功能齐全的项目，并在墙上着陆。关于通过 DMA 与 WS2812B LEDs 聊天的更多信息，请回顾我们的[档案](https://hackaday.com/2016/10/06/driving-16-ws2812b-strips-with-gpios-and-dma/)。

 [https://www.youtube.com/embed/Ix9cpKzIxDA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ix9cpKzIxDA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

