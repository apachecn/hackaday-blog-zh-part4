# C64 用少量零件转动特雷门琴

> 原文：<https://hackaday.com/2022/08/30/c64-turned-theremin-with-a-handful-of-parts/>

特雷门琴因其怪异的声音输出和非接触式演奏风格而广受欢迎。虽然它们通常是使用模拟硬件建造的，但[Linus kesson]决定使用古老的 Commodore 64 制作一个。

该仪器通过测量两个天线与地面之间的电容来工作。当人们在相应的音高和音量天线附近挥动他们的手来改变这些电容时，特雷门琴通过改变其输出的音高和音量来做出响应。

在这种情况下，简陋的 555 被压入服务。它作为一个振荡器运行，其频率根据用户手的位置而变化。当然，音高和音量各有一个，使用夹子和勺子作为天线。C64 然后读取 555 的振荡频率，然后将这些转换成音高和音量数据，以馈入 SID 音频芯片。

[Linus kesson]通过缓慢演绎*奇异恩典*巧妙地演示了构建过程。C64 中的 SID 合成器芯片可以模拟特雷门琴，这里使用的是调制脉冲波声音。这是一个令人印象深刻的构建，我们完全期待在一个大型 chiptune 展会上看到它。我们几乎感到惊讶的是，当时没有人推出 C64 特雷门弹药筒。

我们最近也看到了其他受特雷门琴启发的奇特建筑，比如这个基于灯光的设计。

 [https://www.youtube.com/embed/WZKklJG-UaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WZKklJG-UaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

