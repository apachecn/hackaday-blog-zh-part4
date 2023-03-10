# GitHub 走向无 GUI 化

> 原文：<https://hackaday.com/2020/02/15/github-goes-gui-less/>

Git 是一个方便的工具，我们中的许多人不仅仅在软件开发中使用它。拥有一个基于云的上游存储库也非常有用，但直到现在使用 GitHub——最常见的上游服务器——意味着启动一个网络浏览器，至少对于某些任务是这样。现在 GitHub 发布了一个测试版的[命令行工具](https://github.blog/2020-02-12-supercharge-your-command-line-experience-github-cli-is-now-in-beta/)，用于[操作你的 GitHub repos](https://cli.github.com/) 。

这些工具是早期发布的，所以它们主要关注问题和拉式请求。当然，git 本身会做一些普通的事情，比如克隆和签出——你总是可以在命令行上做这些事情。公告博客帖子中给出的示例列出了带有“需要帮助”标签的所有问题:

```
gh issue list --label "help wanted"
```

我们注意到，在命令行上请求查看问题时，仍然会打开浏览器。工具还为时过早，所以这是让开发人员知道您想要什么或以其他方式影响项目的绝佳时机。

我们有点惊讶，它不只是消耗 git，所以你会使用相同的命令，它只会传递预先形成的命令给 git。当然，如果您对这种东西感兴趣的话，将它编写成一个 shell 脚本包装器是相当容易的。

如果你只把 git 看作是管理源代码修改的一种方式，这是可以理解的，[但是它实际上有各种各样有趣的功能](https://hackaday.com/2017/05/23/stupid-git-tricks/)。