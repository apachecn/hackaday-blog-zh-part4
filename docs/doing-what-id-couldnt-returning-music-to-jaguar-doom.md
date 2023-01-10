# 做我不能做的事:让音乐回归美洲虎末日

> 原文：<https://hackaday.com/2019/08/04/doing-what-id-couldnt-returning-music-to-jaguar-doom/>

虽然世界其他地方基本上已经忘记了雅达利捷豹，但这款慷慨营销的游戏机仍然有一个粉丝群，甚至一些专注的黑客也在努力开发它。[西哈诺·琼斯]就是其中之一，他做了一些很多人认为不可思议的事情:[恢复美洲虎末日港的游戏音乐](https://atariage.com/forums/topic/287323-enabling-music-sound-fx-mixing-within-jaguar-doom-source/?do=findComment&comment=4239037)。

经典射手的捷豹版是 id 软件自己开发的，一般认为是比较好的控制台端口之一。例如，美洲虎控制器上的大量按钮允许玩家直接选择武器，而不是在它们之间循环。不幸的是，在游戏过程中完全没有音乐是一个明显的疏忽，从一个相当坚实的演示中扣除了几分。

造成这种情况的罪魁祸首是捷豹的 DSP 已经被用于数学处理，所以它没有任何周期用于音乐播放。再加上时间紧迫，我可能会减少他们的损失，发布不带游戏音乐的游戏，而不是尝试花更多的时间来设计一个解决方案。为了弥补游戏中音乐的不足，我在幕间休息时加入了著名的配乐，而不是完全去掉。

正如[Cyrano]通过研究 2003 年以来可用的源代码发现的那样，Jaguar 版本的 Doom 中的音效是使用一种叫做“环形缓冲区”的东西播放的:一种循环的固定长度数据缓冲区，它不断地以音频形式输出。有了一块未使用的内存，他可以放入第二个环形缓冲区，在代码的其他地方几乎没有性能影响的情况下向其呈现音乐，然后混合两个缓冲区以获得最终的音频输出。看起来好像我已经有了一些解决方案，但是有足够多的问题迫使他们为了按时发布游戏而放弃了这个想法。

软件黑客并不是捷豹粉丝群唯一可以做的事情，硬件黑客的一个很好的例子是[这个定制的 mod 显示了它在集成单元](https://hackaday.com/2013/11/27/the-atari-jaguar-that-should-have-been/)中使用 CD 插件后的样子。

 [https://www.youtube.com/embed/wNVJrmDN1k8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wNVJrmDN1k8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[迈克·沃森]的提示！