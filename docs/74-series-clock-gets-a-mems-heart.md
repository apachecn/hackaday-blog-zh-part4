# 74 系列时钟获得 MEMS 心脏

> 原文：<https://hackaday.com/2020/01/16/74-series-clock-gets-a-mems-heart/>

[Erik van Zijst]作为一名程序员已经有了很长的职业生涯，但是缺乏对裸机级别发生的事情的理解。在用晶体管构建了几个逻辑门来感受电子设备之后，他开始使用 74 系列逻辑构建一个工作时钟。自然，这是一次相当冒险的经历。

这个项目和许多人一样，都是从试验板上开始的。必不可少的 BCD 计数器和 7 段显示器都有了来源，一切都用五颜六色的连接线连接起来。一个 32.768 KHz 的晶体被压入服务，以产生时钟信号，分频后得到 1Hz 输出，以驱动秒计数器，然后运行整个时钟。[Erik]然后必须学习一些更实用的电子技能，处理时间设置电路的去抖动按钮。

现在时钟已经可以工作了，[Erik]决定更进一步，旨在构建更健壮、更可用的东西。使用 555 创建了自动亮度控制，以运行用于 led 的粗略 PWM 调光器。此外，PCB 设计用于取代临时试验板设置。这导致振荡器出现了[Erik]无法解决的问题。他没有继续走同一条路，而是改变了策略，用一个现代的 MEMS 振荡器取代了石英晶体，解决了这个问题。

它很好地展示了如何从纯粹的逻辑构建一个工作时钟，并提醒我们即使是一个看似简单的设备也可以有多复杂。我们以前也见过其他从零开始的构建，[像这个 777 晶体管时钟](https://hackaday.com/2016/06/01/transistor-logic-clock-has-777-transistors/)、[或者这个吸引人的堆叠设计。](https://hackaday.com/2018/09/06/transistor-logic-clock-gets-stacked-up/)休息后的视频。

 [https://www.youtube.com/embed/RXZeaL9HYxQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RXZeaL9HYxQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/VpXJpEoqJYc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VpXJpEoqJYc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

