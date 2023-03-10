# GlScopeClient:一个许可的远程示波器实用程序

> 原文：<https://hackaday.com/2019/05/30/glscopeclient-a-permissively-licensed-remote-oscilloscope-utility/>

现代数字示波器最方便的事情之一是，您可以在计算机上访问记录的数据，以便稍后进行分析、高级协议调试，或者只是方便远程捕获。问题是软件并不总是理想的。供应商提供的实用程序通常是闭源的，它们试图为每一个*自选*协议和/或功能向您索取一分钱。开源选项有它们自己的问题，从性能限制的设计，到不完整的特性，再到许可限制。面对这些问题，[Andrew Zonenberg]决定亲自动手，创建了 [glscopeclient，一个许可授权的开源远程示波器实用程序](https://github.com/azonenberg/scopehal-apps)。

最终的目标是让你可以使用示波器的前面板远程做任何你通常会做的事情，并在计算机端捕获和分析数据。代码使用模块化架构，允许各种后端与不同的作用域对话。目前，唯一完全实现的后端是 LeCroy scopes，尽管这足以证明这个想法的力量。名字中显而易见的“gl”泄露了秘密——代码使用 OpenGL 进行渲染，这允许以高帧速率绘制一些非常漂亮的图形。

然而，在光滑的外表背后，是一些严肃的调试工具。协议分析仪包括 USB、UART、JTAG、眼图分析，以及带瀑布显示的基于 FFT 的频谱。[代码在 GitHub](https://github.com/azonenberg/scopehal-cmake) 中，大多数公告和讨论似乎都发生在【安德鲁】的 twitter 账户上，你可以关注 [@azonenberg](https://twitter.com/azonenberg) 。这是一项正在进行的工作，但却是一项严肃的工作，是我们将继续关注的事情。

休息之后，你可以看看这个节目的录像。

现在，如果你真的想让 [*对着你的示波器说*，我们也讨论过这个问题](https://hackaday.com/2019/03/03/talk-to-your-scope-and-it-will-obey/)。

 [https://www.youtube.com/embed/hA_oO4o9ns0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hA_oO4o9ns0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

