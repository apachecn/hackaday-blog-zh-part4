# 用最简单的方法从 O-scope 中抓取图像

> 原文：<https://hackaday.com/2019/03/30/grab-an-image-from-your-o-scope-the-easy-way/>

Rigol DS1054Zed 就是你要的示波器。如果你没有示波器，这个示波器有你需要的能力和功能，它很便宜，做硬件黑客的人已经有一个了。这意味着这个示波器有大量的硬件黑客。Zed 的一个小问题是，从屏幕上捕捉图像过于复杂，官方文档需要专用软件和大量的繁琐工作。现在有了一个简单的 python 脚本,它从一个 Rigol 作用域中获取一个屏幕帽。

这个 python 脚本的使用非常简单，只需将 DS1054Z 插入 USB 端口并运行脚本即可。屏幕上的任何内容的 PNG 文件都会出现在你的硬盘上。测试已经在 OS X 上完成，它可能在 Linux 和 Windows 上运行。这是一个简单的工具，做一件工作，荣耀和哈利路亚，人们仍然这样设计工具。

这项工作受到了[cibomahto]，[的启发，他花了一些时间用 Linux 和 Python 控制 Rigol。这项工作将在一个窗口中绘制示波器捕捉到的任何东西，在 Linux 中，但有时你只需要一个示波器上任何东西的屏幕截图；这就是为什么当时有奇怪的惠普望远镜宝丽来适配器。](http://www.cibomahto.com/2010/04/controlling-a-rigol-oscilloscope-using-linux-and-python/)

是的，这是一个完成一项工作的简单工具，但是如果你需要那个工具，你*真的*需要那个工具。[rdpoor]正在寻找一些人来测试它，当然拉请求是可以接受的。