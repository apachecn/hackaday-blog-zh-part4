# 夜曲终极魔法

> 原文：<https://hackaday.com/2021/05/20/terminal-magic-with-notcurses/>

编写一个需要更多活力的命令行程序？课程不够丰富多彩或分辨率不够高？或者您可能希望将演示场景带到命令行中。Notcurses 支持你。演示很棒，看起来它可以推出足够的细节来完成愚蠢的事情，就像将 SNES 游戏的输出直接推送到主机上一样。该库最令人印象深刻的元素可能是，虽然它可以通过具有图形支持的终端仿真器 blit 高分辨率图形，但它也可以在没有安装图形系统的基本 Linux 控制台上工作，方法是使用一些非常古老的技巧。我知道你在想什么:这一切都很好，但它能运行厄运吗？[是的](https://twitter.com/roblogic_/status/1393028449757917184)。休息后回来看演示。

该项目的作者[Nick Black]早在 2019 年就开始了它，并拥有为数不多的贡献者，并声称支持 C、C++、Python 和 Rust。这看起来是一个有前途的项目。它在 SSH 上工作，甚至有鼠标支持。不仅如此，这种美学确实激起了我们对演示场景的热爱，特别是因为它借用了一些技术作为后备像素绘制模式。如果你受到启发，用 notcurses 制作了一个演示，一定要让我们知道！

 [https://www.youtube.com/embed/dcjkezf1ARY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=16&wmode=transparent](https://www.youtube.com/embed/dcjkezf1ARY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=16&wmode=transparent)

