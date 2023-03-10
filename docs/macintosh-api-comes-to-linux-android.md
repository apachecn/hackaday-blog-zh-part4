# Macintosh API 来到 Linux，Android

> 原文：<https://hackaday.com/2019/01/26/macintosh-api-comes-to-linux-android/>

与 DOS、早期版本的 Windows 和大多数* nixes 不同，经典的 Mac 操作系统很怪异。包含在 ROM 中的是绘制窗口、弹出对话框和其他各种与 UI 完全相关的任务的子程序。在其他系统上，这与 BIOS 是分开的，但是在你 80 年代的 Mac 上，所有的东西都放在 rom 中，隐藏在操作系统的深处。这给仿真带来了许多问题；没有 ROM 或者没有真正安装操作系统，你就无法模拟一台旧的 Mac。BeOS——一个很酷但完全被遗忘的操作系统——有一个编程 API 的开源重新实现，对于一台一度拥有 10%市场份额的计算机来说，没有什么比这更好的了。这很奇怪，我们一直在等待有人提出 Macintosh 工具箱的开源重新实现，这个 API 负责从 LoadRunner 到 Shufflepuck 的一切。

现在这一天终于到来了。[高级 Mac 替代品](https://www.v68k.org/advanced-mac-substitute/)是经典 Mac OS 的 API 级重新实现。你现在可以在 Linux 和 Android 上运行经典的 Mac 应用程序，而无需使用苹果 ROM 或苹果系统软件。

高级 Mac 替代品(AMS)是[乔希·巨然]的一个项目，可以在没有苹果 rom 的情况下运行旧的(OS 7 之前的)Mac 软件。在过去的二十年里，Macintosh 模拟器需要苹果 ROM 和/或安装介质，因为 API 调用会重定向到 ROM。与其他仿真项目不同，AMS 不试图仿真硬件，除了 68k 处理器。它只是直接启动到一个应用程序，前端是一个通用的位图终端。这意味着没有操作系统可言，但这也意味着我们终于为经典的 Mac 操作系统获得了 flatpak。

AMS 仍处于非常早期的发展阶段；键盘在某些系统上不能用，在最新版本的 MacOS 上根本不能用。此外，不支持 System 7 应用程序。也就是说，这是 Macintosh 模拟状态的一大进步。如果你想举例说明这有多酷，[去玩俄勒冈小径](https://archive.org/details/msdos_Oregon_Trail_The_1990)告诉我在网页上玩沙狐球或滑翔机有多棒。