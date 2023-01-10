# 你从未见过的游戏男孩是[Sprite_tm]的最新产品

> 原文：<https://hackaday.com/2021/06/29/the-game-boy-as-you-have-never-seen-it-before/>

在 2021 年，向一个孩子解释一个游戏机，他们几乎不知道那个厚重的灰色砖块在过去有多大影响。搜索 YouTube 视频来演示，你可能会找到我们放在休息下面的那个。它从游戏男孩上的经典俄罗斯方块开始，然后转移到超级马里奥世界，然后给我们看刺猬索尼克，最后是末日。所有游戏男孩全盛时期的开创性游戏，有一个小问题。最后三款游戏都不是 Game Boy 游戏，当然也不会在该设备有限的硬件上运行。你们中的大多数人现在不会惊讶地发现，讲述者不是别人，正是[Sprite_tm]，而[他的游戏男孩有着我们见过的最好的树莓 Pi 转换之一](https://spritesmods.com/?art=dmgplus)。

考虑到他之前的工作，我们预计墨盒上有一个 ESP32，以某种方式映射到 Game Boy 显示内存，但事实上，他将原来的任天堂主板换成了一个替代品，在一侧携带 ICE40 FPGA 来处理任天堂硬件，在另一侧携带 Pi Zero 来完成繁重的工作。插入一个 Game Boy 盒式磁带，它会模拟原始的磁带，你永远不会怀疑它不是真的，但插入一个非 Game Boy 盒式磁带，它会将一个标识符传递给 Pi，Pi 会启动一个脚本来运行适当的 Pi 代码。所以马里奥和索尼克游戏运行在基于 Pi 的模拟器上，而毁灭战士在 Pi 上本地运行。它给人一种无缝游戏体验的感觉，这正是它的魅力所在。

这个项目当然具有我们对 Sprite 的期望，快速浏览这些页面将会看到大量以前的例子。最近的一个是[微型工作 DEC VT100 终端，包含一个仿真 PDP 小型机](https://hackaday.com/2021/01/18/a-miniature-vt102-running-a-miniature-pdp11/)。

 [https://www.youtube.com/embed/EpbRpu-3eZs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EpbRpu-3eZs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

