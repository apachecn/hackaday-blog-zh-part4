# 这是他们如何给 EDSAC 电脑编程的

> 原文：<https://hackaday.com/2018/09/28/retrotechtacular-heres-how-they-programmed-the-edsac-computer/>

当你为你的计算机编写程序时，不管它是台式计算机、微控制器还是超级计算机，你都有可能使用软件工具来帮助你完成工作。高级语言、编译器、连接器、汇编器、调试器和代码库已经变得如此集成，以至于在许多情况下你几乎意识不到它们的存在。实际上，这个庞大的工具链将会是计算机。但是第一批计算机程序员没有这些奢侈品。他们必须手工组装自己的二进制文件，手工检查它们，并通过猜测失败时发生了什么来调试它们。

[![EDSAC I, 1948, W.Renwick with 5 hole tape reader and Creed teleprinter. Copyright Computer Laboratory, University of Cambridge. Reproduced by permission. [CC BY 2.0 UK]](img/7cd12e50dc2c47c035d0aea1c01054ea.png)](https://hackaday.com/wp-content/uploads/2018/09/edsac99-34.jpg) 

EDSAC I，1948，W.Renwick 带 5 孔磁带阅读器和 Creed 电传打字机。剑桥大学计算机实验室版权所有。经许可转载。[[CC BY 2.0 UK](https://www.cl.cam.ac.uk/relics/archive_photos.html#Copyright_Licencing%20Copyright%20and%20Licensing%20information)]

[EDSAC](https://en.wikipedia.org/wiki/Electronic_delay_storage_automatic_calculator)(**E**electronic**d**elay**s**storage**a**automatic**c**alculator)是英国剑桥大学运营的第一台计算机，也是 20 世纪 40 年代末建成的全球首批少数几台计算机之一。这是 1951 年电影《T21》的主题，你可以在下面找到。该视频最初是为一次会议制作的，播放了该机器的创造者莫里斯·威尔克斯教授 1976 年的介绍和旁白。它并没有带领我们完成机器本身的设计，相反，它专注于编程所需的工作流程。

## EDSAC 编程的繁琐过程

为了说明编程过程，一群现在自称为计算机科学家，但当时可能自称为数学家的人，在辛苦地手工汇编代码之前，将一个公式分解成子例程。连接过程也是由秘书手工完成的，他把代码输入电传打字机，以便传送到穿孔带上。当需要一个库函数时，她就从文件柜中取出包含它的那卷磁带，然后用磁带复制机把它添加到程序中。最后，检查完成的磁带，并将其添加到由墙上一排挂钩组成的作业队列中。永远不要再抱怨你的工具链笨拙了！

最初的 EDSAC 在为大学服务并产生了商业版本 LEO 后，于 20 世纪 50 年代末退役，LEO 成为第一台用于商业用途的计算机。然而，EDSAC 的故事并没有就此结束，因为在本世纪，位于 Bletchley Park 的国家计算机博物馆的一个团队开始将 EDSAC 作为一个展览来重现。幸运的是，该团队的一名成员在最近的电磁场黑客营做了一个关于他们工作的演讲，你也可以在下面找到。

## 建造 EDSAC 的忠实复制品

托尼·艾比给了我们这部机器的历史和它的结构描述，接着是他们重建这部机器的过程。你可能会对演讲中一些意想不到的事实感到惊讶。例如，虽然 EDSAC 中使用的所有试管仍然可用，但它们的底座已经不可用。等效物来自中国，但团队成员不得不用牙钻对其进行修改。

他们还需要制造 20 世纪 40 年代风格的管状底盘，而这个问题的解决方案恰好就在前方。布莱奇利是现代米尔顿凯恩斯的一部分，这是一个战后的新城镇，也是另一个著名名字的所在地:[马歇尔放大器](https://marshall.com/)。电子管放大器的制造方式惊人地相似，因此它们接受了制造挑战。虽然不是所有新 EDSAC 的零件都是原装的。存储器在 1949 年使用水银延迟线，但在 2018 年的娱乐中，计算机使用镍线和现代组件的延迟线。托尼承认，即使这样也造成了问题，有一个使用微控制器的模拟器。

你可以在国家计算机博物馆看到修复的 EDSAC。我们[在 2016 年](https://hackaday.com/2016/09/13/review-the-national-museum-of-computing/)参观过，你可以看看我们的评论。同时，如果你是一个 FPGA 向导，[你甚至可以有一个自己的虚拟 EDSAC](https://hackaday.com/2017/10/05/learn-fpga-programming-from-the-1940s/)。

 [https://www.youtube.com/embed/6v4Juzn10gM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6v4Juzn10gM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/3g6UqEsHgNE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3g6UqEsHgNE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



剑桥大学计算机实验室版权所有。经许可转载。[ [CC BY 2.0 UK](https://www.cl.cam.ac.uk/relics/archive_photos.html#Copyright_Licencing%20Copyright%20and%20Licensing%20information)