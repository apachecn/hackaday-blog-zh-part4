# C++编译器面向 Web

> 原文：<https://hackaday.com/2020/12/21/c-compiler-targets-the-web/>

这是目前的一个普遍问题。你有一段 C 或 C++代码。也许是旧代码。或者你可能更喜欢用 c 来构建你的想法的原型，但是，不可避免的是，现在有人想让你的代码在 Web 浏览器中运行。实现这一点的选项最近扩展了很多，其中一个可能性是[cherep](https://github.com/leaningtech/cheerp-meta)，一个处理高达 C++ 17 的开源编译器，可以输出到 WebAssembly、JavaScript 或 asm.js。

该编译器可免费用于 GPLv2 项目。如果你不开放自己，看起来你必须和它的创造者学习技术公司达成协议才能使用 Cheerp。

传统上，您会使用 Emscripten 来做这样的事情。根据该项目的网站，Cheep 生成的 WebAssembly 比 Emscripten 更快更小，如果编译成 JavaScript，它有几个优点。例如，他们声称拥有更好的动态内存处理、更高效的 DOM 访问和更好的 JavaScript 互操作性。

可以理解的是， [Hello World 示例](https://github.com/leaningtech/cheerp-meta/wiki/Getting-started#hello-world)有点乏味，但确实展示了一些允许直接访问浏览器的特殊功能。他们确实指出，如果你不担心性能，你可以忽略这一点，使用像`printf`或`cout`这样的东西。如果你想做一些严肃的事情，一个更好的起点是[乒乓游戏示例](https://github.com/leaningtech/cheerp-meta/wiki/Cheerp-Tutorial:-Mixed-mode-C++-to-WebAssembly-and-JavaScript)。

如果您还没有跟上 [WebAssembly](https://hackaday.com/2019/04/04/webassembly-what-is-it-and-why-should-you-care/) 的进度，我们可以帮助您开始。如果你认为这些在嵌入式系统中没有应用，我们会推荐你去 [Olaf](https://hackaday.com/2020/08/30/olaf-lets-an-esp32-listen-to-the-music/) 。