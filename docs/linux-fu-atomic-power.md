# Linux Fu:原子能

> 原文：<https://hackaday.com/2022/09/26/linux-fu-atomic-power/>

人们很清楚虚拟机的威力。如果你想做一些危险的事情——比如入侵内核——你可以创建一个虚拟机，给它拍快照，搞砸几次，恢复它，你的主计算机就不会错过任何一个节拍。但是有时候你需要的只是一点点视角的转变，而不是一台完整的虚拟电脑。例如，您正在构建一个新的启动盘，您想假装它是真正的启动盘并进行一些更新。为此，有一个 Linux 命令`chroot`，它可以让你临时打开那些认为文件系统的根与真正的根在不同位置的进程。问题是，很难管理一堆`chroot`环境，这就是为什么他们创造了[原子](https://github.com/AtomsDevs/Atoms)。

该系统可以与几种常见的发行版一起使用，您可以通过 Flatpak 安装它。这意味着，举例来说，你可以启动一个 shell，它认为自己在 Ubuntu 下运行的是 Gentoo 或 Centos Linux。

[![](img/4f3f599d43e646377cd605666936391f.png)](https://hackaday.com/wp-content/uploads/2022/09/setup.png)

Creating an atom is easy

使用这个工具很容易。一个简单的屏幕让你选择几个选项。第一次使用某个特定的图像时，需要几分钟时间来下载所有内容。

最终，您将得到所有`chroot`环境的列表。选择其中的一个(最初，是唯一的一个)会给你一个屏幕，在这里你可以浏览文件，暴露一些挂载点，改变 chroot 的名字，或者清除它。您也可以直接在选定的环境中打开控制台。

[![](img/f7424b05ee34ad29facff10dd9cee96a.png)](https://hackaday.com/wp-content/uploads/2022/09/details.png)

You can perform many actions on an atom from the GUI

在主屏幕上有一个“汉堡包”菜单，允许你做一些全局的事情，比如设置偏好。例如，你可以移动物品的存放位置。您也可以删除不打算再次使用的图像。

这是你不能从命令行做的事情吗？当然不是。但是这是一种很好的方式，可以很好地组织特定发行版的许多`chroot`环境。

我们希望你可以很容易地为自己创造定制的原子，但是如果有，我们没有看到。当然，整个事情都在 GitHub 上，所以如果你真的有动力的话，你可能会知道如何去做。我们还注意到，除了一些简单的选择之外，您无法控制大多数底层主机文件系统如何映射到 atom。有些情况下，您可能希望映射其他内容，但不清楚如何实现这一点。

如果你需要更多的隔离，考虑[容器](https://hackaday.com/2018/09/05/intro-to-docker-why-and-how-to-use-containers-on-any-system/)。如果你想要[快速开发 docker 图片](https://hackaday.com/2022/06/21/linux-fu-docking-made-easy/)，我们也谈到了这一点。