# esp32 专案的迷你图

> 原文：<https://hackaday.com/2020/06/06/sparklines-for-your-esp32-projects/>

在典型的微控制器项目中，我们可能只能使用相对较小的屏幕。信息显示可能是一个挑战，但它可能会通过使用 Arduino 框架的用于 Espressif 处理器的 ESParklines 库变得更容易。

[迷你图](https://en.wikipedia.org/wiki/Sparkline)是一个简单的线形图，没有注释(如轴或单位),适合文本流。今天，他们大多与统计学家[爱德华·塔夫特](https://www.edwardtufte.com/tufte/)联系在一起，如果你以前没有遇到过他们或 Tufte，那么我们建议你享受自学。

这是一个非常简单的库，并且附带了示例代码。有用的是，它维护了一个自己的数据缓冲区，允许简单的更新，除了例子之外，我们还在文件夹下放了一个 YouTube 视频，显示了随着更多信息的加入而演变的图表。不过，我们对一件事很好奇，它被宣传为 ESP8266 或 ESP32 的 ESP 库，但我们在那里找不到任何 ESP 专用的代码，我们友好的 ESP 专家也找不到。我们错过了什么吗？如果你能提供一些线索，评论如下。

 [https://www.youtube.com/embed/Pvfijfrt5HI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Pvfijfrt5HI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

