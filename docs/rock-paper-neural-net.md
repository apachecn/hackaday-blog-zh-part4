# 石头，纸，神经网络

> 原文：<https://hackaday.com/2019/07/09/rock-paper-neural-net/>

你可能认为石头剪子布的游戏只是随机的机会，但那不是真的。石头剪子布有一个策略，事实上是多个策略，最好的人类玩家可以始终如一地击败街上的任何一个笨蛋。但是电脑呢？[Paul] [用一个可以在石头剪刀布中打败你的小钥匙链来回答这个问题](https://github.com/PaulKlinger/rps-rnn)。

这是一个神经网络，你需要训练一个神经网络，那么[保罗]是从哪里得到这些数据的？roshambo.me 提供了数千种纸石头剪刀游戏，并在超过 85，000 种人类游戏以及大约 10，000 种模拟游戏上训练了网络。石头剪刀布根本不是一个复杂的游戏，整个神经网络都存储在 ATtiny1614 微控制器上。计算是以浮点形式完成的。这就是这个项目的非计算密集型程度。

建立一个神经网络是一回事，但把它放在一个方便的钥匙链外壳中是另一回事。这个漂亮的设备安装在比 2032 纽扣电池大一点的 PCB 上，并封装在 3D 打印的外壳中。按钮也是 3D 打印的，巧妙应用了光纤作为 led 的光导管。最终结果是比石头剪子布的随机机会稍微好一点的东西，并展示了一些矩阵编程技巧。看看下面的视频。

 [https://www.youtube.com/embed/iuTKBHW0OaU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iuTKBHW0OaU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

