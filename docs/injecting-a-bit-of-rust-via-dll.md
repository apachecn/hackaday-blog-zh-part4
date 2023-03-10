# 通过 DLL 注入一点铁锈

> 原文：<https://hackaday.com/2022/07/11/injecting-a-bit-of-rust-via-dll/>

曾经因为软件包缺少你想要的功能而沮丧过吗？在最好的情况下，软件是开源的，你可以修改代码然后重新构建。但是在很多情况下，软件是闭源的。在[比石灰更快]的案例中，他找到了一个不支持控制器的 SNES 模拟器(Snes9X)来展示这项技术。所以稍微锈了一下，[他写了一些代码，可以通过 DLL 注入](https://fasterthanli.me/videos/getting-good-at-snes)注入仿真器。

这是一个展示这项技术的精彩教程。他首先创建了一个 rust 项目，该项目使用了[DLL-注射器](https://crates.io/crates/dll-syringe)箱(依赖管理的 Rust 版本)。这个机箱完成了将 DLL 注入目标进程的大部分繁重工作。剩下的旅程是浏览 Windows 文档和实现特性的一个很好的过程。DLL 只是读取控制器，然后将正确的输入发送给程序。最后，[比石灰更快]有一个很棒的注入 DLL，我们在注入环境中学习 Rust 和调试有一段美好的时光！

自从[我们上次讨论 DLL 注入](https://hackaday.com/2015/02/28/beating-super-hexagon-with-opencv-and-dll-injection/)已经有一段时间了，很高兴看到这个过程是如何发展的。休息后的视频。

 [https://www.youtube.com/embed/Yr9qy9reLCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Yr9qy9reLCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

