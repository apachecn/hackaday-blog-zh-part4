# POLF:复古 3D 游戏仅使用一个角色显示

> 原文：<https://hackaday.com/2021/10/18/polf-retro-3d-game-uses-only-a-character-display/>

有逆向计算的痒吗？[David Given]也是，幸运的是，他编写了 POLF:一款为准将宠物设计的第一人称 3D 游戏，仅使用系统的 40×25 文本模式角色显示来实现视觉效果。这是一个了不起的成就，考虑到 80 年代的电脑拥有 32 kB 的内存，甚至没有图形显示。

![](img/fd524c0a9cb815bb56154f8e6b64860f.png)

Each level has an 8×8 layout.

POLF 的每一关都是一个迷宫般的小房间，玩家的目标是玩一种介于台球和高尔夫球之间的游戏，目的是将圆形的“球”移动到方形的“洞”中。使用[光线投射](https://lodev.org/cgtutor/raycasting.html)渲染 3D 视图，这是一种使用有限资源高效绘制可行 3D 透视图的方法。光线投射只能做这么多，但是作为一种方法，它在它的限制范围内非常有效，而且有[有用的教程展示了这个过程](https://hackaday.com/2021/09/13/ray-casting-101-makes-things-simple/)。

[这个项目的 GitHub 库在这里](https://github.com/davidgiven/polf)，它应该运行在任何 40 列屏幕的 PET 上，至少有 16 kB 的 RAM。观看下面嵌入的视频中的实际操作。(提示:屏幕底部指南针标题下的小条形图代表玩家与球和洞对象的接近程度。)

 [https://www.youtube.com/embed/wO5euiOo4kk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wO5euiOo4kk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

