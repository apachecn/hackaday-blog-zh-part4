# 甜蜜的流是由这些组成的:在命令行上创作音乐

> 原文：<https://hackaday.com/2020/03/19/sweet-streams-are-made-of-these-creating-music-on-the-command-line/>

创作音乐有无数种方式。在最简单的形式中，它甚至不需要任何设备，正如 beatboxing 或 capella 所证明的那样。如果我们转向计算机，情况也差不多:音频编程语言和通用高级语言以及声音合成软件一样早就出现了。就像物理设备一样，多亏了`sed`，这些都不是特别必要。是的，*`sed`，这位优秀的老流编辑，正如【laserbat】在她的音乐生成脚本中显示的[。](https://github.com/laserbat/bach.sed)*

 *以巴赫 c 大调前奏曲 1*的[缩略版](https://github.com/laserbat/bach.sed/blob/master/bach.min.sed)和[全注释版](https://github.com/laserbat/bach.sed/blob/master/bach.sed)为例，[laserbat]使用乐谱的字符串表示作为脚本的起点，以及每个转换音符波长的查找表。从这里，她生成每个音符的固定长度 PCM 方波信号，通过 ALSA 的`aplay`或 SoX 的`play`按原样传输到声卡。为了使事情足够简单，她在这里保持在可打印字符的范围内，使用 space 和 tilde 分别作为低值和高值，以这种方式同时提供尽可能高的音量。*

 *这个概念本身当然不是什么新东西，它是如何工作的`.au`和`.wav`文件，以及[这些小 C 行](https://hackaday.com/2011/11/01/annoy-your-sound-guy-even-more/)。虽然固定的音符持续时间带走了[laserbat]版本中的一些平滑度，但添加可变持续时间可能对`sed`实现来说是一个太多的暗示，尽管[我们在过去肯定见过一些更复杂的脚本](https://hackaday.com/2020/01/12/maze-solving-via-text-editing/)。

[通过[r/编程](https://www.reddit.com/r/programming/comments/fi31wf/you_can_use_gnu_sed_to_generate_music_heres/)**