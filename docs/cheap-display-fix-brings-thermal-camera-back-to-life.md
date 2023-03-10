# 廉价的显示器修复让热感相机重现生机

> 原文：<https://hackaday.com/2022/11/20/cheap-display-fix-brings-thermal-camera-back-to-life/>

谈到电子设备的可维修性，很大程度上取决于原始制造商的帮助程度。有些通过出版详细的维修手册和出售备件使维修变得非常容易。其他人对一切都保密以保护他们的知识产权，甚至把一个本应简单的修复变成了逆向工程的考验。当[BuyItFixIt]得到一台显示器损坏的 FLIR 万用表-热感相机组合仪器[时，他很快发现 FLIR 坚定地站在“我们所有的设计都是最高机密”的阵营中，甚至不会告诉他他们使用了什么样的显示器。](https://www.youtube.com/watch?v=3IQgyN5OzNs)

[BuyItFixIt]没有被吓倒，他把仪表拆开，试图找出问题所在。来自微处理器的信号似乎正常地到达显示器，所以故障出在屏幕本身的某个地方。显示器的零件号没有在网上返回任何有用的结果，但全球速卖通确实有一个非常相似的显示器，零件号略有不同。这种显示起初似乎工作正常，但仪器随后陷入了启动循环。

与 FLIR 不同的是，替换显示器的供应商很乐意提供数据手册，甚至为最初的 FLIR 器件提供了一份数据手册。有了这些新信息，[BuyItFixIt]能够推断出新屏幕没有输出一个处理器期望看到的信号，导致它自己重置。一个简单的解决方法是将相应的引脚连接到来自背光控制器的 PWM 信号，这欺骗了 CPU，使其认为连接了正确的显示器。

在这种情况下，12 美元的显示屏和一根电线足以让一台昂贵的仪器起死回生，但事情并不总是那么简单。更复杂的机器[可能需要数周时间来调试](https://hackaday.com/2022/04/18/the-epic-journey-of-repairing-an-hp-9830a-desktop-computer-from-the-1970s/)，即使零件是可用的。如果没有，你甚至需要[设计自己的](https://hackaday.com/2019/03/03/designing-custom-lcds-to-repair-retrocomputers/)。

 [https://www.youtube.com/embed/3IQgyN5OzNs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3IQgyN5OzNs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

