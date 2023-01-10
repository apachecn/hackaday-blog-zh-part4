# 这个细长的字钟使用激光蚀刻来保持简单

> 原文：<https://hackaday.com/2021/02/21/this-slimline-word-clock-uses-laser-etching-to-keep-things-simple/>

从我们得到的提示来看，单词钟的受欢迎程度最近似乎开始下降了。但是回到高峰世界时钟，我们看到了几十个设计，一些比另一些更好。这个简单而优雅的单词钟似乎受益于所有的现有技术，使设计尽可能简单，同时仍然看起来很棒。

[t0mg]的主要工具是激光切割机，这是保持设计简单的一个很好的选择。单词时钟的棘手部分是让“单词搜索”矩阵干净地执行，我们已经看到了一切，从[激光切割木材](https://hackaday.com/2018/12/26/word-clock-dont-need-no-stencil-font/)到[喷墨打印](https://hackaday.com/2019/03/09/rgb-word-clock-doesnt-skimp-on-the-features/)，甚至[商业生产的 PCB](https://hackaday.com/2019/03/27/leds-shine-through-pcb-on-this-tiny-word-clock/)，用于这项工作。[t0mg]转而选择在一块玻璃上喷漆，并用激光蚀刻掉字符，从而获得极高的文字质量。蚀刻玻璃的下侧也有保护油漆层的好处，同时给完成的时钟一个光滑的表面，看起来真的很好。在模板下面是 MDF 层，其中包含 Neopixel 条并充当光导，而 ESP32 和 RTC 则执行计时和 LED 驱动任务。[t0mg]用一个漂亮的 web 界面来设置时钟、改变颜色和执行维护功能，完成了时钟。下面的视频展示了正在使用的软件。

我们真的认为这个时钟看起来很棒，对于那些有激光切割机的人来说，这似乎是一个建造自己的时钟的好方法。

 [https://www.youtube.com/embed/WF_X5soabm0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WF_X5soabm0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

