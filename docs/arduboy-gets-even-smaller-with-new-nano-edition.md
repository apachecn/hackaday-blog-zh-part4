# 新的 Nano 版本使 Arduboy 变得更小

> 原文：<https://hackaday.com/2021/02/05/arduboy-gets-even-smaller-with-new-nano-edition/>

Arduboy 的卖点之一是 slim [Kevin Bates]能够获得 Arduino 兼容的游戏系统，当你意识到它最初是作为电子名片的设计而出现的时候，这可能就不那么令人惊讶了。但是与最近发布的 Nano 版本相比，它还不如老派的“砖块”游戏男孩。

[![](img/bc5c19cd6c4d20ff6c1adaf3cf96789d.png)](https://hackaday.com/wp-content/uploads/2021/02/ardunano_detail.jpg) 现在要明确的是，[凯文]并不打算将这些投入正式生产。虽然听起来裸露的多氯联苯可能会在不久的将来出售。这只是一个实验，看看他能在多大程度上缩小核心 Arduboy 硬件，同时保持它不仅可以玩，而且代码与全尺寸版本兼容。虽然“可玩”在这种情况下可能有点主观，但休息后的视频清楚地证明了它的完全功能。

在 3D 打印的外壳内，是为 Arduboy 提供动力的同一款 ATmega32U4，一个 64×32 0.49 英寸的有机发光二极管显示屏和一个 25 毫安的小型电池。甚至还有一个微型压电扬声器用于哔哔声和滴答声。所有的引出线都保持不变，所以现有的代码可以直接移过来，尽管屏幕现在是通过 I2C 连接的。[Kevin]已经发布了电路板的原理图，以符合 Arduboy 项目的一般开放性质，尽管现在他决定保留电路板文件，直到 Nano 是否有商业前景明朗为止。

我们以前见过缩小 Arduboy 的尝试，[最明显的是缩小到可以放入 Dreamcast 视觉存储单元](https://hackaday.com/2019/02/04/arduboy-brings-new-life-to-dreamcast-vmu/)的程度，但 Nano 肯定会提高(或者降低？)的酒吧相当。

 [https://www.youtube.com/embed/CWUFwAB7mBQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CWUFwAB7mBQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

