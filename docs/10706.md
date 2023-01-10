# 新的视频系列:树莓 Pi Pico 和 RP2040 深潜与 Uri Shaked

> 原文：<https://hackaday.com/2021/07/29/new-video-series-raspberry-pi-pico-and-rp2040-deep-dive-with-uri-shaked/>

如果你一直生活在没有互联网接入的岩石下，树莓 Pi 基金会今年通过[树莓 Pi Pico](https://hackaday.com/2021/01/20/raspberry-pi-enters-microcontroller-game-with-4-pico/) 同时进入了硅销售和微控制器游戏。它体积小，功能强，价格只有区区 4 美元。你现在肯定有一两个了，对吧？但是你对它的功能了解多少呢？

或者也许你还没有，但它在你的清单上。无论哪种情况，你都可以马上开始了解它们，因为[Uri Shaked]的 *[Raspberry Pi Pico 和 RP2040 Deep Dive](https://hackaday.io/course/178733-raspberry-pi-pico-and-rp2040-the-deep-dive)* 课程最近已经从 HackadayU 的神圣大厅中释放出来。他甚至建立了一个模拟器来配合它。[尤里]是一个伟大的教练，我们相信，如果你需要一个萨尔萨舞蹈老师，他也掌握了双倍。

这门课从 2021 年 5 月开始，为期五周，每节课大约一小时。唯一的先决条件是对位数学有一个基本的了解，但是在上面链接的 class IO 页面上有相关的资源。

每堂课都组织得非常好，内容丰富。在第一堂课的[中，【Uri】开始构建](https://www.youtube.com/watch?v=Duel_Oaases)[一个活文档](https://link.wokwi.com/pi-pico-class)，其中包括课程议程、所有使用和提到的资源的链接、代码示例以及适用的汇编指令。它基本上是一个教学大纲加上一大堆东西。[Uri]还在[花了大量时间阅读 RP2040](https://datasheets.raspberrypi.org/rp2040/rp2040-datasheet.pdf) 令人难以置信的详尽的 649 页数据表，并花了一点时间阅读更短的[入门指南](https://datasheets.raspberrypi.org/pico/getting-started-with-pico.pdf)。如果您认为数据表是不可理解的，那么在您看到[Uri]的使用并仔细阅读之后，您可能会在第一堂课结束时改变您的看法。

 [https://www.youtube.com/embed/OLV-TSRTTE8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OLV-TSRTTE8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



第一类开始时是一种宏观的高级介绍，但[Uri]很快就使用 Pico 仿真器进入了实质性内容——例如如何通过直接写入输出引脚的存储寄存器来使多个 led 闪烁，而无需大量代码。同样，您可以从多个输入中读入数据。我从观看第一个课程中学到了很多，包括一个简单的解决 I/O 引脚的方法和[一个我从未见过的非常巧妙的 GitHub 技巧](https://github.com/conwnet/github1s)。

随着课程的进行，您将深入 RP2040，沉浸在系统架构、硬件寄存器和 ARM 汇编语言的基础知识中。最后，您将沉浸在可编程输入/输出(PIO)的知识中，这是 RP2040 芯片的一项独特而令人兴奋的功能，允许您创建更多的硬件接口。

 [https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PL_tws4AXg7avNexvQxkfxfEBtvTtBi6Tu](https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PL_tws4AXg7avNexvQxkfxfEBtvTtBi6Tu)



2021 年的 HackadayU 可能会在夏天结束，但不要担心。与此同时，[去 Hackaday.io](https://hackaday.io/courses) 上看看后面的目录，在那之前找些有助于充实时间的东西。