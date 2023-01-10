# 增加一个协处理器来帮助 SNES 游戏减速

> 原文：<https://hackaday.com/2019/08/18/adding-a-co-processor-to-help-snes-games-with-slowdown/>

Gradius III 的超级任天堂港口因其接近街机原版而闻名，其大型、明亮和丰富多彩的图形。然而，由于控制台硬件的限制，该端口在游戏过程中也经常变慢，尤其是在后面的部分。[熊伟]破解了这个游戏，[制作了一个补丁版本的 ROM，使用协处理器来消除这些问题](https://github.com/VitorVilela7/SA1-Root)。

在《格拉迪乌斯》中看到的速度变慢对 SNES 玩家来说并不少见，当几个精灵同时出现在屏幕上时，那个时代的许多游戏都会受到影响。这部分是由于任天堂选择了老化的 CPU，据说是为了在这个想法被放弃之前保持 NES 向后兼容。在需要显示下一帧时无法完成任务，硬件会跳过帧，让处理器在继续之前赶上。这被认为是前面提到的减速。

在 SNES 生命的后期，游戏开始在游戏盒中使用额外的芯片来增强主机的性能。其中之一是 SA1，它是一个与主 CPU 具有相同内核的协处理器，只是时钟频率更高。通过使用它，游戏有更多的时间在下一帧之前运行逻辑和图形操作。熊伟所做的是将格拉迪乌斯 III 的那些部分移植到 SA1 T1，本质上使它就像以前的任何其他增强弹药筒一样。

与我们之前看到的通过给 SNES 更长的消隐时间来超频不同，这种方法可以在真正未经修改的硬件上完美地工作。你可以在休息后看到他努力的结果，特别是在第二阶段，第二个视频中几个气泡充满了屏幕。

 [https://www.youtube.com/embed/pmJyQiL9wYg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pmJyQiL9wYg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/hIcoVXi3UZQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hIcoVXi3UZQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Via [Ars Technica](https://arstechnica.com/gaming/2019/05/28-years-later-hacker-fixes-rampant-slowdown-on-snes-gradius-iii/) ，感谢达米安的提示！]