# 蛇与梯子:Python 中的 Game Boy 模拟器

> 原文：<https://hackaday.com/2020/04/26/snakes-and-ladders-game-boy-emulator-in-python/>

如果一个游戏机是你童年的一部分，你可能不止一次梦想着和它一起度过你的整个学校生活。嗯，他们不得不为此再等几年，但最终在 2015 年，[Asger]、[baekalfen]和[troelsy]为一个大学项目用 Python 开发了一个 Game Boy 模拟器，让这个梦想变成了现实。然而，它并没有就此停止，模拟器自此发展成为一个成熟的开源项目 PyBoy，它的[刚刚达到 1.0 版本发布](https://github.com/Baekalfen/PyBoy)。

由于它最初是一个学术项目，他们三人必须相应地进行研究，因此他们编写的关于 Game Boy 内部功能和仿真器的背景和理论在一份与源代码一起发布的报告中进行了总结。仍然有一些工作要做，可悲的是还没有实现声音支持，但在大多数情况下，它的功能是完全的，让你成功地播放[你自己提取的卡带](https://github.com/Baekalfen/PyBoyCartridge)，或者你拥有的任何 ROM 文件。

作为一个模拟器，你也可以在调试模式下运行时检查它的内部生命，并在你玩的时候观察精灵、磁贴和数据，另外还可以做一些很酷的事情，比如反向播放模拟，如下面的剪辑所示。更重要的是，你可以在你自己的 Python 脚本中加载实例，并开始为你的游戏编写你自己的机器人——在之前，我们已经[在《NES》中看到了这一点。如果你想真正深入到游戏男孩的世界，你绝对应该看一下](https://hackaday.com/2018/12/16/ai-bot-plays-castlevania-so-you-dont-have-to/)[的 33c3 关于它的演讲](https://hackaday.com/2020/03/14/the-ultimate-game-boy-talk/)。

> [查看 imgur.com 的帖子](https://imgur.com/nr9VWwe)