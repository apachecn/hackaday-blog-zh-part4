# 使用 ESP8266 构建更智能的烟雾报警器

> 原文：<https://hackaday.com/2019/07/26/building-a-smarter-smoke-alarm-with-the-esp8266/>

现代黑客使用许多工具，这些工具的工作原理是将东西加热到极高的温度，因此烟雾报警器确实是一件必备的设备。但在一个似乎一切都变得越来越智能的时代，有些人可能会想，即使是我们的安全装置也能从加入物联网中受益。有兴趣尝试改进经典的烟雾报警器， [[Vivek Gupta]抓起一个 NodeMCU 并开始编写一些代码](https://github.com/vikkey321/notsodumbsmokedetector)。

现在，在你跳到评论里开始敲打键盘之前，让我们把我们在这个问题上的立场说清楚。**不要试图制造自己的烟雾报警器**。说真的。只有一种特殊的傻瓜才会把他们的家，甚至他们的生活，托付给一个 5 美元的开发板和一些他们从互联网上复制粘贴的 Arduino 源代码。也就是说，作为一个纯粹的学术实践，研究如何利用现代互联网微控制器为最普通的家用设备添加有用的功能当然是值得的。

在这种情况下，[Vivek]正在试验一种烟雾报警器的想法，如果出现假警报，可以通过您的家庭自动化系统使其静音。他使用的是谷歌助手和 IFTTT，但代码可以适用于你内部使用的任何方法，让你所有的小工具都在同一个虚拟页面上。在硬件方面，测试系统只是一个连接到蜂鸣器和 MQ2 气体传感器的 NodeMCU。

那么它是如何工作的呢？如果探测器在[Vivek]做饭时响起，他可以告诉谷歌助手他正在做饭，这是一场虚惊。这使蜂鸣器静音，但在此之前，系统会回复一条信息，询问他在厨房的技能。这是一个简单的生活质量改善，当然不难想象这个想法如何扩展到通知你一个可能的情况，即使你不在家。

我们已经看到一系列的小问题如何发展成威胁生命的情况。如果你要进行类似的实验，确保你有一个“哑”烟雾报警器作为备用。

 [https://www.youtube.com/embed/j9lKQJRmcAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j9lKQJRmcAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

