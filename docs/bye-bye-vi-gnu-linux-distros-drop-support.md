# 拜拜 Vi: GNU/Linux 发行版支持

> 原文：<https://hackaday.com/2019/04/01/bye-bye-vi-gnu-linux-distros-drop-support/>

如果您和我们一样是在 Unix 系统中长大的，那么听到这个消息您会感到很遗憾:vi，这个在这 40 年里为我们服务得如此之好的高贵的文本编辑器，正在从许多 GNU/Linux 系统中消失。在撰写本文时，GNU/Linux Mint、Debian、Ubuntu 和 OpenSUSE——五个最流行的 GNU/Linux 发行版中的四个——都宣布他们将不再把“vi”编辑器作为基础安装的一部分。对于我们这些从穿孔卡片时代开始并仍然认为文件是行的集合而不是字节流的人来说，这是一个重大的打击。但是，我们都可以感到欣慰的是，至少现在，这些系统上的精简版 vim(VI 的同义词)将继续从包存储库中获得。

我们并不完全清楚这样做的原因，但是从我们在 GNU/Linux 邮件列表上看到的情况来看，令人困惑的模态界面和新手(以及许多经验丰富的用户)不知道如何保存文件和退出程序的事实似乎影响了我们的决定。还提到了随着 GNU/Linux 越来越受欢迎，预期的支持变化。随着用户群的扩大，包括不太懂技术的个人，越来越少的人能够解决他们经常出现的启动问题，这是 vi 的主要用例。取代自助模式的将是一个支持基础设施，用户可以把他们的机器带到“GNU/Linux 天才”那里，他们将为他们解决问题。

## 战争结束了

这一举动基本上结束了 vi 和 GNU Emacs 之间的编辑器战争，这场战争从 1980 年代中期就开始了。GNU Emacs 不是作为大多数(任何？)发行版，所以这个声明让编辑们回到了平等的地位，至少就发行版而言是这样的。要在您最喜欢的 Linux 系统上获得 vi 版本，您需要显式地安装它，就像 GNU Emacs 用户似乎一直在做的那样。我们不希望两个阵营之间的敌对情绪完全消退，但我们不禁想知道，考虑到替代编辑器将被发运，能量是否会更好地应用于其他地方。

## 辞旧迎新

那么，随着这两个热门的退出，新 GNU/Linux 中的默认编辑器会是什么呢？我们与一家大型商业发行公司(你知道是哪一家)的内部人士进行了交谈，他告诉我们，微软的 Visual Studio 代码(重命名为 GNU/Visual Studio 代码)的一个版本将随其 GNU/Linux 操作系统的所有未来版本的基础安装一起发布，实际上取代了 vi。虽然我们最初对这一决定感到惊讶，但引用的理由很有道理。首先是受欢迎程度。Visual Studio 代码在 [2018 Stack OverFlow 开发者调查](https://insights.stackoverflow.com/survey/2018/)中排名第一，超过 10 万名受访者中有 34.9%的人表示他们使用过该编辑器。Vim 用户仅占 25.8%，Emacs 仅占 4.1%。很多 JavaScript 开发人员都不会错。

我们的消息来源还提到了微软最近对开源的尝试，包括 GNU/Visual Studio 代码编辑器本身(在麻省理工学院许可下发布)，Windows 计算器代码的突破性发布[，](https://hackaday.com/2019/03/12/finally-an-open-source-calculator/)和[他们最近对 GitHub 的收购](https://hackaday.com/2018/06/05/microsoft-confirms-github-acquisition/):

> 到目前为止，微软已经**接受了**开源，并继续**扩展**他们已经参与的项目。我迫不及待地想知道接下来会发生什么。

我们同意。