# 游戏男孩成为超级游戏男孩，有一对 Pis

> 原文：<https://hackaday.com/2022/01/14/game-boy-becomes-super-game-boy-with-a-pair-of-pis/>

对于 90 年代的任天堂迷来说，超级游戏男孩是超级任天堂的必备组件，它允许玩家在你的电视上玩游戏男孩游戏。它不仅允许在大屏幕上玩四色点阵游戏，而且让你不用花一大笔钱买 AA 电池就能玩那些最喜欢的游戏。虽然后来的掌上电脑如 PSP 甚至任天堂 Switch 能够毫无问题地将视频直接输出到电视上，但最初的游戏机需要 SNES 的处理帮助，或者正如[Andy West]向我们展示的那样，[它也可以从现代微控制器](https://community.element14.com/challenges-projects/element14-presents/project-videos/w/documents/27407/episode-531-game-guy---the-unportable-game-boy?CMP=SOM-YOUTUBE-PRG-E14PRESENTS-EP531-COMM)获得帮助。

[![](img/e0ebd1e86149251c68c11ac4aa7af934.png)](https://hackaday.com/wp-content/uploads/2022/01/gameboynes_detail.jpg)

Testing the design before installing it in the NES case.

在这种情况下，额外的处理能力来自 Raspberry Pi Pico，它足够小，可以轻松放入捐赠的 NES 盒中，而且功能强大，可以直接处理 VGA。对于视频数据输入，Pico 通过电平转换器连接到 Game Boy 主板上的视频引脚。主板还连接到第二个 Pico，它处理来自 NES 控制器的控制器输入。此时需要进行一些奇特的转换，因为尽管控制器布局非常相似，但它们由各自的控制台完全不同地处理。

随着所有技术工作的完成，[Andy]可以对构建进行最后的润色了。这些措施包括确保电源按钮，状态指示灯和复位按钮都正常工作，并恢复 NES 的情况下，完成一些自定义的“游戏家伙”图形，以匹配游戏男孩的原始设计。我们也赞扬在这个版本中使用了原始的游戏机硬件，这甚至使[Andy]和他的妻子能够通过连接线与另一个游戏机玩马里奥博士的面对面游戏。如果你正在寻找一种更简单的方式在原始硬件上玩游戏，而不是在你的钱包里烧一个洞购买 AA 电池，看看[这个游戏男孩恢复使用锂电池代替](https://hackaday.com/2015/01/01/game-boy-with-lithium-batteries-and-usb/)。

 [https://www.youtube.com/embed/ypGMU5lLjeU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ypGMU5lLjeU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢 [Hackaday Discord 服务器](https://discord.com/invite/NkbHrAW7NG)的【BaldPower】和【adistuder】发来这篇文章。