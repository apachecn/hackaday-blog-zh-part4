# 美丽的自由形式的 LED 时钟重现 20 岁的周末项目

> 原文：<https://hackaday.com/2020/05/09/beautiful-free-form-led-clock-recreates-20-year-old-weekend-project/>

在 Hackaday，我们喜欢好的时钟项目。如果这是一个艺术化的自由雕塑，那就更好了。但是告诉我们，这也是二十年前的一个经典项目的新旋转，我们为此欣喜若狂。一个典型的例子:[保罗·加拉格尔的 LED 钟的美丽再现重复了 2000 年初最初作为周末项目制作的一个。

等等等等。等一下。

*Ted 解开翻领上的麦克风，从椅子上站起来*

好的，亲爱的读者，如果你允许的话，我们将以一种稍微不同的方式来做这件事。通常我应该用黑客日的声音来写，但这个项目对我来说有个人意义，所以我想打破一些规则。你看，最初的时钟项目是我的——很久以前我在一个周末做的，PCB 上的“2/13/2000”日期就是证明——我很荣幸[Paul]会选择我的项目作为灵感。

[![](img/e66f4ca6985553b9256ebcf429dc77e2.png)](https://hackaday.com/wp-content/uploads/2020/04/original-led-clock.jpg)

Original Clock Project dated 2/13/2000

在这座钟诞生 20 周年之际，我在 Twitter 上发了一条帖子来纪念这件事，[保罗]捡起球，带着它跑了起来。你可以[在这里](https://twitter.com/tedyapo/status/1228024969902379009)看到最初的 Twitter 帖子。他只需要家里蚀刻的单面电路板的照片，就可以对相对简单的设计进行逆向工程，然后重新创造出风格。

该设计采用 PIC16F84 微控制器。这是第一批真正受到业余爱好者欢迎的微控制器之一，其关键特征是串行编程算法，允许简单的自制程序员和闪存。如果我没记错的话，我最初的程序员用的是 PC 的并口。我可能把它放在某个盒子里了。12 个 led 中的每一个都通过独立的电阻从单独的 GPIO 线路驱动，而 32.768 kHz 晶体用作时基。最后，两个按钮允许您设置小时和分钟。

你如何在这样的显示器上表现三只不同的手？在这种情况下，每只手以不同的速度眨眼。小时 LED 是稳定的，秒 LED 比分钟 LED 闪烁得更快。休息之后，你可以在[Paul 的]视频中查看，并欣赏他的布局的美丽简洁。

因为他能够准确地重新创建电路，所以[Paul]能够插入运行时钟的原始汇编代码。事实上，Microchip 仍然生产 PIC16F84，他们的最新工具对这样的遗留代码没有问题——它只是工作。

 [https://www.youtube.com/embed/oq4bqvXI8DM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oq4bqvXI8DM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



尽管我们的[巡回雕塑比赛](https://hackaday.com/2019/01/15/twelve-circuit-sculptures-we-cant-stop-looking-at/)已经结束，hack aday*一直*在寻找像这样有趣的自由形式的作品，所以如果你已经制作了一个，或者刚刚在野外发现了一个，[给我们发个短信](https://hackaday.com/submit-a-tip/)。

[谢谢艾米丽]