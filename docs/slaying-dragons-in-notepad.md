# 记事本中的屠龙

> 原文：<https://hackaday.com/2020/05/27/slaying-dragons-in-notepad/>

我们都有自己喜欢的文本编辑器，并愿意通过任何必要的手段捍卫它高于所有其他编辑器的优越性。然后还有记事本。但是 Notepad 可能缺少文本操作功能，但它作为游戏平台的不显眼特性弥补了这一点。是的，你没看错，而[sheep solution]用在记事本中运行的基于文本的冒险游戏[提供了证据。](https://sheepolution.com/blog/gamedev/how-i-made-a-game-played-in-notepad/)

以开玩笑地想知道这样一个游戏看起来会是什么样子开始的东西，最终作为它的答案成为了一个实际的实现。在幕后，一个使用[love 框架](https://love2d.org/)用 Lua 编写的脚本——他还为此创建了[一个广泛的教程](https://sheepolution.com/learn)——监控组成游戏世界的几个文本文件的状态。每个位置都是一个单独的文本文件，可以在记事本中打开，显示游戏的当前状态，用文本和 ASCII 艺术讲述故事，并为玩家提供选择。通过修改和保存这些文本文件来玩游戏，然后脚本处理这些文件，通过简单地用新状态更新这些文件的内容来推进游戏。休息之后看看游戏的预告片，感受一下它的样子。

不幸的是，记事本本身不会在内容改变时自动重新加载文件，因此为了提供更流畅的游戏体验，[Sheepolution]修改了开源实现 Notepad2 来解决这一问题，并将其捆绑为游戏可执行文件的一部分。最初，他甚至将动画添加到 ASCII 图形中，但最终决定不使用其中的大部分，以避免持续的磁盘写入和由此导致的竞争情况。

当然，这不是文本编辑器中的 [Game Boy emulator，它可能不像](https://hackaday.com/2019/03/06/the-strangest-gameboy-emulator-weve-seen-yet/)[记事本的最新功能](https://hackaday.com/2018/05/08/windows-notepad-now-supports-unix-line-endings/)那样具有开创性，但看到[对成熟工具的替代使用](https://hackaday.com/2018/09/13/a-whole-other-kind-of-graphical-programming/)总是很有趣。

 [https://www.youtube.com/embed/qcdMVoE4mJM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qcdMVoE4mJM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



(对于 Linux 用户来说，这款游戏可以用 Wine 来玩，但是你可能需要从记事本中手动加载游戏世界的文本文件。一旦可执行文件启动，您将在`C:\users\<user>\Application Data\And yet it hurt\Game\`目录中找到这些文件。)