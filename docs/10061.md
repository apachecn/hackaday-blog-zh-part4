# 四个伺服手指比你能更好地演奏西蒙

> 原文：<https://hackaday.com/2021/05/10/four-servo-fingers-play-simon-better-than-you-ever-could/>

记得西蒙吗？我们当然有。西蒙——就像“西蒙说……”——来自 20 世纪 70 年代电子游戏的前沿，它使用四个按钮、彩色灯光和简单的音调作为记忆游戏的基础。为了进入下一轮，玩家必须记住灯的特定顺序，并重放该模式。它令人惊讶地令人上瘾，至少对那个时代来说是这样。

对于那些从来没有真正进入过 Simon groove 的人来说，不用担心，这款经典游戏现在已经完全自动化了。虽然有很多方法可以用来与游戏交互，但[ido roseman]采用了显而易见的——在我们看来也是最好的——技术，用伺服控制的手臂模拟了人类玩家的手指按压。每个手臂上都有一个光敏电阻，可以记录它上方的按键发出的光；Arduino 会感应并记录灯光序列，然后驱动伺服手指进行重放攻击。手指的反应并不准确，这可能会引起问题——如果我们没记错的话，西蒙对按键的速度有些挑剔，至少在较高水平的游戏中是这样。

总的来说，我们真的很喜欢这个，不仅仅是因为怀旧的因素。这些年来，我们已经对西蒙进行了很多再创作，包括[一个舞蹈革命版本](https://hackaday.com/2015/07/24/ddr-ing-a-simon-game-with-a-raspberry-pi/)，但是很少尝试自动化。还有一个疯狂的想法:用一个机器学习系统来取代重放攻击，该系统通过随机按键并观察结果来计算出如何玩西蒙，这难道不是很有趣吗？

 [https://www.youtube.com/embed/93AUhSyVjkg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/93AUhSyVjkg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

