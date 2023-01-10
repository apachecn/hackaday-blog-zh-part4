# 脉冲发生器用 STM8 完成这项工作

> 原文：<https://hackaday.com/2020/10/01/pulse-generator-does-the-job-with-an-stm8/>

当使用硬件时，无论是修复还是重新构建，通常都需要测试一些东西。取决于你在做什么，如果你不能把正确的信号传到正确的地方，这可能是容易的，也可能是痛苦的。为了消除这个令人沮丧的问题，[【威尔科尔】建造了一个在实验室使用的有用的脉冲发生器。](https://www.instructables.com/id/Pulse-Generator/)

[WilkoL]指出，从历史上看，产生不同长度和频率的脉冲的工作将由 555 个定时器来完成。虽然这是一种非常完美的方法，但是人们希望采用不同的方法来增加现代硬件所能提供的灵活性。脉冲发生器是围绕 STM8 微控制器构建的；毫无疑问，这是这个时代不同寻常的选择。[WilkoL]特别提到了该器件，因为它的成本极低，定时器硬件功能强大，非常适合这项工作。

结合 ST7735 TFT LCD 屏幕，并为提高效率而采用裸机编程，最终项目安装在一个项目箱中，可控制频率和脉冲长度——不多也不少。脉冲长度能够从 250 纳秒到 90 秒，频率从 10 兆赫到 2 兆赫，这是一个工具，应该是舒适的测试一切从伺服到机械计数器。

当然，如果你需要降低到皮秒的时间尺度，雪崩脉冲发生器可能更适合你的速度。休息后的视频。

 [https://www.youtube.com/embed/I4hL2p_5-Vg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I4hL2p_5-Vg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

