# Pathio:来自 E3D 的新型 3D 切片器

> 原文：<https://hackaday.com/2019/02/24/pathio-new-3d-slicer-from-e3d/>

拥有一个优秀的文字处理器实际上不会帮助你写出下一本畅销小说。这可能会让事情变得更简单，但是如果你有一部很棒的小说，如果有必要的话，你可以用蜡笔在纸巾上写下来。一台优秀的 3D 打印机并不是制作优秀 3D 打印品的全部。这在很大程度上取决于你开始使用的型号和称为切片器的软件。你有几个选择，现在你又多了一个: [PathIO](https://pathio.xyz/hello-world/) ，一个由 E3D 赞助的切片器，正在测试中。你可以在下面看到一个关于它的功能的视频。

该软件有一些粗糙的边缘，正如你可能会从测试版期待的那样。尽管 Octoprint 集成即将推出，但切片器并不直接将 Gcode 输入打印机。开发者说他们正在关注全新的切片引擎。根据他们的网站，传统切片器会立即将模型切割成 2D 切片，然后决定如何根据外壳和填充物实现每个切片。Pathio 在 3D 空间工作，并声称这有利于产生正确的壁厚和增加自支撑几何形状。

另一个即将推出的功能是一种新的支撑方法，使用 Z 运动产生微小的牙齿来支撑上面的层。这看起来是一个很棒的想法，尽管显然有一些缺陷阻止了它出现在当前版本中。

我们喜欢在一个任务中对零件进行分组，每个组都有自己的设置。切片器也提供基于 Jinja2 的脚本。除了强大的语言之外，脚本编辑器还提供语法着色和自动完成功能。

路线图上也有很多，包括机器之间的云同步——过去当我们在不同的工作站上有稍微不同的切片配置文件时，这一直困扰着我们。好消息是切片器可以在 Windows、Linux 和 OSX 上工作。坏消息是，它对电子也是如此，所以这将会激怒一些人。然而，切片引擎本身是原生的 C++，所以这应该会减轻您在使用 electronic 时可能遇到的一些问题。然而，它确实意味着另一个应用程序会在你的计算机上安装另一个 Chromium 和其他工具的私有副本。

虽然 PathIO 还有很长的路要走，但它已经有了一个令人印象深刻的开始。我们不得不承认，现在我们根据我们正在做的事情更换切片器。Cura 与一些模型配合得更好，Slic3r 与其他模型配合得更好。如果有一个能在不同的工作站上保持更新并能全面做好工作的切片机就太好了。我们会看到它如何发展。

在过去的几年里，我们已经看到不止一款[新型切片机](https://hackaday.com/2017/11/10/icesl-is-a-cool-slicer/)上市。我们也看到了有着特定目标的老年切片师的[特别版](https://hackaday.com/2017/06/12/prusacontrol-the-beginners-slicer/)。我们甚至看到有人想要[编写自己的切片器](https://hackaday.com/2017/03/01/diy-3d-slicer-is-a-dynamo/)，如果那是你的事情的话。

 [https://www.youtube.com/embed/jIyajEtFY28?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jIyajEtFY28?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

