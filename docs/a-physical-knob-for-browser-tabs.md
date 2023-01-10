# 浏览器选项卡的物理旋钮

> 原文：<https://hackaday.com/2019/04/30/a-physical-knob-for-browser-tabs/>

如果你像我们大多数人一样，你现在有大约 20 个浏览器标签打开。如果有一种方法可以通过物理界面在这些选项卡之间移动会怎么样？[这就是[佐伊]所做的，这也发生在有史以来最好的笔记本电脑上。](https://hackaday.io/project/165285-webtuner)

这个构建的硬件只是一个 Arduino 和一个旋转编码器，没有问题。Arduino 上的固件只是读取编码器，并通过串行端口发送一两位数据。当您将它连接到 Firefox 扩展时，这个构建变得很有趣，Firefox 扩展允许您从 USB 或串行端口获取数据，并且有一个很好的 API 来访问选项卡。将所有这些放在一起，你就有了一个旋钮，可以滚动浏览所有打开的标签页。

当你考虑到还有一个 3D 打印支架，旨在连接到 Thinkpad X220，有史以来最伟大的笔记本电脑时，这种构建变得非常好。轻轻一按旋钮，你就可以滚动浏览所有标签。如果你同时阅读三个、四个或五个文档，或者如果你只是编辑视频并试图同时浏览你的笔记，这是很方便的。这是一项伟大的发明，我们正在等待它成为键盘和鼠标的标准设备。看看下面的视频。

 [https://www.youtube.com/embed/nNiJmV_KFPg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nNiJmV_KFPg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

