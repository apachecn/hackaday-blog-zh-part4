# 俄罗斯方块在分裂皮瓣去 Brrr

> 原文：<https://hackaday.com/2021/03/07/tetris-on-split-flap-go-brrr/>

这看起来几乎不可能，但是工程师集体和分离式显示器供应商[Oat Foundry]能够在一天的时间内在 10 x 40 的分离式显示器上构建俄罗斯方块的工作实现。休息后看看视频。

这个项目在细节部门有点人手不足，但我们知道[Oat Foundry]从[Timur Bakibayev]的用 Python 开源实现俄罗斯方块的[开始，并修改了`draw`函数以在分瓣显示上工作。正如你可能已经猜到的，最大的障碍是刷新率及其对可玩性的影响——特别是在玩家在扔掉棋子之前旋转棋子的紧张时刻。分裂襟翼从开到关翻转很快，但翻转回开需要在所有其他角色之间来回一次。](https://levelup.gitconnected.com/writing-tetris-in-python-2a16bddb5318)

我们认为这对于一天的构建来说是很好的工作。如果他们走得更远，我们希望看到和[Oat Foundry]一样的东西被实现:一个高分追踪器和下一个作品的预览。

没有翻盖显示器？是的，我们也是，但是我们有电视。打开电视[看看这个纳米级的俄罗斯方块](https://hackaday.com/2020/02/28/a-tetris-to-be-proud-of-with-only-a-nano/)。

 [https://www.youtube.com/embed/WRfOCW2GmFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WRfOCW2GmFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Via [reddit](https://www.reddit.com/r/EngineeringPorn/comments/lxnkph/tetris_programmed_on_an_old_school_airport/)