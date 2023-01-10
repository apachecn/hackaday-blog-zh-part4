# 电子骰子是微控制器编程入门

> 原文：<https://hackaday.com/2022/05/27/electronic-dice-is-introduction-to-microcontroller-programming/>

到目前为止，我们大多数人都熟悉 Arduino 平台。这是进入微控制器世界的一种廉价且相当容易的方式。对于很多项目来说，没有必要超出这个范围，除非你想了解更多微控制器的内部工作原理。[Cristiano]有兴趣扩展他的一些知识，所以他决定使用 PIC 微控制器而不是他更熟悉的 Arduino 平台来构建他的电子骰子。

因此，这个项目是为那些不具备 Arduino 那样的手持设置，希望进一步深入微控制器世界的人而设立的。为了满足骰子对随机数的需求，使用了 PIC 的随机数生成器，但增加了内部定时器种子的随机性。当一个水银倾斜开关向该装置发出它已经翻转的信号时，计时器启动，经过一些计算后，一个单一的数字显示在七段显示器上。

虽然表面上看起来很简单，但该项目附带了一个关于 PIC 系列微控制器编程的深入指南，并有一个初学者项目通常不会看到的抛光，包括使用水银倾斜开关，使其具有复古氛围。关于如何构建这样的项目的一些其他技巧，[看看这个关于如何为你的项目构建电源的指南](https://hackaday.com/2010/11/20/beginner-concepts-powering-your-projects/)。

 [https://www.youtube.com/embed/TU3mP62WcNA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TU3mP62WcNA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

