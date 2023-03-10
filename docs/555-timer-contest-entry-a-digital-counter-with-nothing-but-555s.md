# 555 计时器竞赛参赛作品:一个只有 555 的数字计数器

> 原文：<https://hackaday.com/2022/01/06/555-timer-contest-entry-a-digital-counter-with-nothing-but-555s/>

BOM 上有一个 555，你永远不知道你会得到什么。在一个版本中有 40 个多功能定时器芯片，你可能会得到一些完全意想不到的东西，比如[这个基于 555 的 8 位数字计数器](https://hackaday.io/project/183172-an-8-bit-binary-counter-made-from-555-timer-chips)。

这个是通过[Astronomermike]来找我们的，他选择只用 555 和少量无源器件制作一个数字电路，作为他参加当前 555 计时器竞赛的参赛作品。无处不在的定时器芯片并不完全是数字应用中想到的第一个芯片，但它确实包含一个 SR 锁存器，只需要一点说服就可以成为 JK 触发器。他最初设计的触发器将成为电路的核心，由一对 555 和一堆“或”门和反相器组成——符合竞赛规则，但不符合其精神。幸运的是，555 也是一个很好的反相器，加上一些二极管电阻或门，基本的计数器模块就诞生了。

下面的视频显示了设计和构建，以及故障诊断兔子洞的行程。8 位计数器的每个半字节阶段用 10 个 555 占据一个完整的试验板；整个 40 芯片串实际上工作，看起来很酷。

说实话，这正是我们在构思今年的 555 比赛时所想的那种事情，所以对于[天文学家]来说，这是一个很好的突破。要想知道人们为这种持续提供的芯片找到了什么其他用途，或者想在 1 月 10 日截止日期前参赛，请前往竞赛页面。

 [https://www.youtube.com/embed/uKf5XAka9AI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uKf5XAka9AI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

