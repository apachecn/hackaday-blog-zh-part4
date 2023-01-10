# 微控制器研究刀片

> 原文：<https://hackaday.com/2020/02/02/microcontroller-studies-the-blade/>

剑道是一种日本武术，用一种特殊的剑练习。虽然这不是一把特别锋利的剑，因为“剑刃”本质上是一段竹子。出于这个原因，剑道练习者必须依靠正确的形式和技术，以确保他们的练习尽可能有效，康乃尔大学的学生[伊曼]和[魏晨]制作了一个[剑道训练器，帮助剑士们学习剑术](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2019/isn7_wz349/isn7_wz349/isn7_wz349/index.html)。

该项目的核心是 PIC32 微控制器，连接到一组三个压电传感器和一个 LSM9DS1 惯性模块。三个压电传感器连接到头盔上，惯性模块连接到剑上，传感器一起工作来确定攻击的位置以及它是否有足够的强度被认为是“好”的攻击(剑道的规则超出了本文的范围)。然后，教练可以计算所有的信息，并在一个小屏幕上向用户提供反馈。

虽然武术相关的构建似乎相对罕见，但我们确实在 2011 年发现了一个类似的项目，名为[虚拟唤醒](https://hackaday.com/2011/10/14/improving-sports-performance-with-a-kinect/)，它使用当时流行的 Kinect 来跟踪动作。不过，这个基于 PIC32 的项目似乎更彻底一些，因为它在计算机使用的信息中包含了罢工的强度，而且启动成本可能更低！

 [https://www.youtube.com/embed/8xJTHIGiG9A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8xJTHIGiG9A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

