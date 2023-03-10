# Remoticon 视频:Meta_Processing 是文本和块编程的混搭

> 原文：<https://hackaday.com/2021/01/05/remoticon-video-meta_processing-is-a-mashup-of-text-and-block-programming/>

很少有人想在眨第一只 LED 之前发明宇宙。当然，如果有足够的兴趣，很多人会深入到原子级技术，然后重新建立自己的方式。但是当你第一次让你的眼睛眨的时候，有一种不可思议的东西，知道如何写 makefiles 在那次经历中不起作用。现在把它应用到使用智能手机作为无线接口的项目中…我们能让它变得多简单？

[![](img/013f949ef4f07afa4bcaa1bffde2ce1f.png)](https://hackaday.com/wp-content/uploads/2021/01/meta-processing-code-translation.jpg)

Meta_Processing can translate the instructions into any of 14 languages

Jose David Cuartas 正在努力回答这个问题，[在 Hackaday Remoticon 期间举行的这个元处理研讨会](https://www.youtube.com/watch?v=50xgwdB8T0U)上向我们介绍了他的进展。[元处理](https://github.com/hiteclab/Meta_Processing)是一个基于[处理](https://processing.org/)的 IDE 你可能已经猜到了——这种编程语言为那些想在不成为软件禅宗大师的情况下完成视觉上有趣的事情的人打开了更高层次的功能。这里的“Meta_”部分是指它现在可以通过非常有限的输入来完成，并且可以在不同的口语之间互换。

方法是将文本编程和块编程语言的精华融合在一起。通过这种方式，您不需要键入新的行，只需单击鼠标添加它们，并从列表中选择要在该行上使用的指令。这意味着你不需要记住指令，避免代码中的错别字。该说明的文档将显示在 IDE 的底部栏上，以帮助您获取参数。更有意思的是，既然您选择了指令，那么选择 IDE 的 14 种可用语言中的任何一种都将更新您的“代码”,将其翻译成新的语言。

在研讨会上，Jose 用令人惊讶的少量代码演示了许多有趣的例子，包括音频、视频和用户输入，视频包含在下面。IDE 甚至在网络上生成了一个服务器，这样你写的应用程序就可以被智能手机加载。它支持通过数字读/写、模拟读和伺服控制与 Arduino 兼容设备通信。这个项目甚至有一个名为 [Meta_Javascript](https://github.com/hiteclab/Meta_Javascript) 的分支，能够使用类似 REST 的 API。

人们用许多不同的方式学习。拥有这样的选项来帮助人们快速进入 blinky 是打破理解和使用计算机的障碍的一个很好的方式。

 [https://www.youtube.com/embed/50xgwdB8T0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/50xgwdB8T0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

