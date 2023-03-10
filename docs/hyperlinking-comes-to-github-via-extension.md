# 超链接通过扩展来到 GitHub

> 原文：<https://hackaday.com/2019/06/14/hyperlinking-comes-to-github-via-extension/>

如果你正在浏览 GitHub，打开某个项目的源代码，看看它是如何工作的，这是非常诱人的。代码视图易于阅读，但是查看器缺少一个重要的特性:单击包含的文件并找到它的能力。 [Octolinker](https://octolinker.now.sh/) 扩展修复了这个疏忽。

如果你想在不安装扩展的情况下尝试一下，有一个[模型演示](https://octolinker-demo.now.sh/OctoLinker/live-demo/blob/master/index.js#LO2)可用。即使这个演示想让你点击特定的东西，如果你不遵守规则，它仍然会做正确的事情，把你带到 GitHub 上的代码或者一个适当的页面。您甚至可以用演示 URL 替换 github.com，并在任何没有扩展的 GitHub 页面上试用。

该工具支持至少 20 种语言，尽管我们困惑地看到 [C 和 C++不在其中](https://github.com/OctoLinker/OctoLinker/issues/521)。开发者声称你的源代码不会被这个扩展发送到你的浏览器之外。根据该网站的说法，如果你在私有存储库上使用 Octolinker，你还必须提供一个 GitHub API 令牌，这也不会被发送到你的浏览器之外。

代码(当然是在 [GitHub](https://github.com/OctoLinker/OctoLinker) 上)有一个插件架构，所以添加你选择的语言应该很容易。如果你渴望在 GitHub 中获得源代码的弹出工具提示，请查看 [OctoHint](https://github.com/pd4d10/octohint) 。

GitHub 似乎在被微软收购后安然无恙。如果你想关注你的 GitHub 属性，总有[这个项目](https://hackaday.com/2013/10/16/monitor-github-activity-with-an-rgb-led-matrix/)。