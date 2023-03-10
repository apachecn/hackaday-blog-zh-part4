# 蜡烛工厂自动化历险记

> 原文：<https://hackaday.com/2019/01/10/automating-a-candle-factory-michale-schuldts-adventures-in-manufacturing-automation/>

你考虑过制造蜡烛吗？不一定是自己制造，而是如何在小规模工业环境中制造？这是 Michael Schuldt 非常关心的事情，因为他正在努力实现简单的手工蜡烛生产过程的自动化。

这不仅仅是一个有趣的主题，但制造自动化的话题是我们都可以借鉴的。这是他在最近的 Hackaday Superconference 上的[制造自动化冒险演讲](https://www.youtube.com/watch?v=YvKTW2bO_kI)的主题。让我们开始吧，看看这是怎么回事！

## 一个简单的过程能有多复杂？

蜡烛的制作过程非常简单，一个盛有熔化蜡的漏斗被放置在传送蜡烛罐的传送带上方，蜡从上方被分配到罐子中。料斗需要定期重新填充，所有任务都由操作员执行。

[![A candle plant ready for automation.](img/7227d430dfba606d18f313204ed62e8b.png)](https://hackaday.com/wp-content/uploads/2019/01/candle-plant.jpg)

A candle plant ready for automation.

迈克尔的第一个原型用气动元件自动化了机器，并用软件攻击整个过程，用一个 MicroPython 循环保存所有可能的功能。他发现这种方法的问题无疑是许多工程师都在努力解决的问题:它很快变得难以操作。整体解决方案没有达到他的基本标准:可靠、可调试、可修复、易于使用。本质上，这个教训是硬件多，软件少。

有一些明显的简化，用为简单任务构建的硬件替换与简单任务相关的多余软件。例如在蜡烛工艺中，当一个简单的开关就足够了时，在软件中有一个蜡罐选择步骤是没有意义的。他意识到，他正在复制常见的现成控制组件，如定时器或 PID 控制器，他的解决方案是放弃大型软件，生产一系列单一功能的 PCB，他称之为[控制砖块](https://hackaday.io/project/162158-control-bricks)。这些都是独立的单元，有自己的显示器和界面，处理特定的任务，并被设计成以链的形式按顺序运行，每个单元通过链传递控制给下一个单元。可以把它想象成作为硬件模块执行的算法的框图。

## 硬件框图

通过这种方式，他创建了一个通用工具包，解决了简单流程自动化的问题，因此值得更详细地研究一下。每个砖块具有一组公共接口、用于与其他砖块连接的链输入和输出、必要时的传感器输入、以及可用于触发继电器或类似装置的活动输出。每个模块上的处理器都是 ATmega328，选择它是为了方便，因为他手头有一批这样的处理器。

[![Three of the process automation bricks, delay, counter, and while functions.](img/348c72720ceb956da30838995f3ca339.png)](https://hackaday.com/wp-content/uploads/2019/01/schuldt-blocks.jpg)

Three of the process automation bricks, delay, counter, and while functions.

可以创建许多可能的砖块来满足所有可能的功能，但是到目前为止，他只创建了蜡烛自动化任务所需的选择。有一个带旋转编码器的进程延迟模块，用于设置时间；一个“while”模块，用于在传感器条件为真时设置输出；一个进程计数器模块，用于在进程每次经过时增加计数；还有一个“stop-start”模块，用于暂停和恢复进程。循环可以简单地通过将链的输出连接到其输入来实现，并且停止-开始砖块通常是链中的第一个。他指出，每次系统运行时都必须手动输入过程参数，而不是在软件中设置，但他认为对于相对简单的过程来说，这应该不是问题。

这种模块化的过程自动化系统并不是全新的，事实上，在继电器驱动的现代可编程逻辑控制器的祖先中也可以找到类似的想法。但是，对于我们的社区来说，拥有一个如此方便实验的现成设计是一个有趣的发展，迈克尔的发现故事应该为任何面临自动化任务的人提供有趣的教训，即使他们不采用他的解决方案。

 [https://www.youtube.com/embed/YvKTW2bO_kI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YvKTW2bO_kI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

