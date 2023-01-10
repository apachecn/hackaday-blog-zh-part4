# 这种负强化键盘可能会让你震惊

> 原文：<https://hackaday.com/2021/01/28/this-negative-reinforcement-keyboard-may-shock-you/>

如果没有科迪隆夫人的中学打字课，我们就不会有今天。尽管她可能想这么做，但她从来没有使用负强化来提高我们的打字速度或技巧。如果这些 IBM Selectrics 能像[3DPrintedLife]的[可怕的、令人兴奋的打字员训练键盘](https://www.youtube.com/watch?v=yxUM_wt-jB4) (YouTube，嵌入下方)那样训练有素，我们这些桀骜不驯的青少年可能会学得更快。

这种键盘使用 capsense 模块和神经网络来检测用户是在触摸打字还是只是在狩猎和啄食。如果你做错了，每次你啄 T 或 Y 键时，你都会被恶作剧电击笔的内脏电击。哦，只是为了好玩，顶部有一个 20 V 的 LED 灯条，它应该阻止你用随机和刺眼的闪光灯低头看你的手。

二十四个键通过手指的使用以三个为一组进行连接，例如 Q、A 和 Z 连接到同一个 capsense 模块。这些都和灯条连在一起。[3DPrintedLife]在 capsense 模块之间遇到了很多串扰，因此他们通过用大量正确和不正确的类型数据训练 TensorFlow 模型，在软件中解决了这个问题。

我们喜欢触摸屏上的小仪表，它可以一目了然地显示您在触摸打字部门的工作情况。当仪表向左移动时，你知道你要大吃一惊了。[3DPrintedLife]甚至内置了一些利用疼痛来促进打字更快更准的游戏。休息后看看构建视频，但不要说我们没有警告你闪光灯的问题。

电击笔的秘密是一个微型回扫变压器，就像 CRT 电视中使用的那种。找一个全尺寸的反激式变压器，你就可以为自己打造一个手持高压电源。

 [https://www.youtube.com/embed/yxUM_wt-jB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yxUM_wt-jB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

