# 大型音频可视化泵与音乐

> 原文：<https://hackaday.com/2022/05/13/big-audio-visualizer-pumps-with-the-music/>

频谱分析仪是创造与音乐合拍的激动人心的视觉效果的好方法。[pyrograf]想要一个大的作为展示品，所以开始动手做他们自己的东西。

ESP32 微控制器作为构建的核心，其高时钟速率和双核使其成为这项工作的最佳选择。来自麦克风的音频被放大并输入到 ESP32 的模拟输入端。然后，ESP32 上的 Core 0 对输入音频进行快速傅立叶变换，以确定每个频带中的能量。然后，FFT 的结果被传递到内核 1，内核 1 用于计算所需的动画，并将它们传输到一系列 WS2812B LEDs。

然而，这个版本真正的亮点在于实际的构造。大块的丙烯酸树脂充当发光二极管的扩散器，照亮光谱显示器的每个部分。将大像素尺寸与 led 上平滑的 30 Hz 刷新率结合起来，结果是一个相当大的频谱分析仪，看起来确实很实用。

[这些年来，我们也看到了一些类似的版本](https://hackaday.com/2021/02/22/led-spectrum-visualizer-driven-by-raspberry-pi/)。休息后的视频。

 [https://www.youtube.com/embed/Vy4BbQ_T4lo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Vy4BbQ_T4lo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

