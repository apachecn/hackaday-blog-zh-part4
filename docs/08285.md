# 你电脑的老式控制面板

> 原文：<https://hackaday.com/2020/11/07/an-old-school-control-panel-for-your-computer/>

自从计算机掌握在程序员手中以来，他们已经提供了频繁的轻度乏味的任务，这些任务是他们的操作员寻求自动化的。谁没有编写过一个 shell 脚本或批处理文件，将一串命令合并成一个命令来节省一点输入时间呢？

但是，即使这种努力也可以通过一个将脚本与物理控件联系起来的硬件附件来减少，在这一努力中[【托马斯】创造了一个美丽的](https://tomas.janco.link/projects/?control-panel.html)。他的控制面板项目模仿了过去坚固的工业面板，在一个坚固的金属外壳中有一系列金属按钮和拨动开关，该外壳来自一个旧的 KVM 开关。

在幕后是一对 I/O 扩展器和一个 NodeMCU 板，它的 ESP8266 负责与主机通信，在主机上有一个守护程序等待它的调用。每个交换机旁边的单独可寻址 led 传达操作状态，交换机触发有用的操作，例如连接到 VPN。所有代码都可以在[一个方便的 GitHub 库](https://github.com/janci007/control-panel/)中找到，你可以在我们放在 break 下面的视频中看到它的运行。

我们很喜欢 Hackaday 的桌面控制面板的想法，事实上[这不是我们带给你的第一个](https://hackaday.com/2015/08/21/you-cant-call-it-a-battlestation-without-this-overhead-control-panel/)。

 [https://www.youtube.com/embed/l2V6jASU0mw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l2V6jASU0mw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

