# 了解旧任天堂的自定义信号协议

> 原文：<https://hackaday.com/2021/07/02/understanding-custom-signal-protocols-with-old-nintendos/>

对于复古游戏来说，原始硬件是无可替代的。然而，随着它的老化，我们很多人都需要找到一些过得去的东西，因为古董硬件不会永远存在。如果一个控制台不能正常工作，模拟器可以帮助我们，但是即使使用模拟器，使用原始控制器仍然是首选。为此，【所有部件组合】[向我们展示了如何在最初的任天堂控制器和 PC](https://www.youtube.com/watch?v=rsPoT7o2iSg) 之间建立自定义接口。

构建从绘制控制器行为开始。SNES 控制器上的按钮并不直接对应于 pin，而是一个时钟在每个定时事件期间锁定特定时刻的所有按钮按压，并将该信息发送到控制台。为了实现这个协议，使用了一个 Adafruit 小饰品，在下面链接的视频中给出了代码的详细解释。从那时起，制造设备本身就是一件简单的事情，因为[所有部件组合]从坏掉的超级任天堂中收集控制器端口，并将所有东西装入一个整洁的盒子中，可以通过 USB 连接到他的 PC。

虽然仅仅因为他丢失了他的 Mega Man 卡盒就让一个定制的任天堂控制器接口运行起来看起来像是一件很大的工作，但是这个构建对理解一个定制的控制器协议有很大的帮助。此外，这里有更多的效用，而不仅仅是玩超级男人；像这样的方法也可以很容易地用于连接其他控制器。我们甚至看到了相反的过程，USB 设备在任天堂 64 上工作。

 [https://www.youtube.com/embed/rsPoT7o2iSg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rsPoT7o2iSg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

