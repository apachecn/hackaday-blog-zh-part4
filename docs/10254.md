# 网络组装、音乐合成和数学之美

> 原文：<https://hackaday.com/2021/05/28/web-assembly-music-synthesis-and-the-beauty-of-math/>

自从微处理器出现以来，电子爱好发生了很大的变化。在此之前，由于缺乏大规模集成电路，杂志上的项目要么非常简单，要么非常复杂。然而，一个流行的项目类型涉及音乐合成。相当简单的电路可以组合成一个复杂的合成器，所以这是一种两全其美的方法。如今，你更有可能在软件中处理音乐合成器，就像[Tim]在 Web 汇编和 C++中创建 [Abelton](https://timdaub.github.io/2020/02/19/wasm-synth/) 时所做的那样。一路上，他学到了很多数学和音乐之间的关系。

[Tim]讲述了他所了解的奈奎斯特定理，以及如何利用缓冲器保持合成数据实时流动。然而，在跨浏览器环境中尝试做所有这些会有一些问题。然而，`AudioWorklet`类似乎得到了广泛的支持，而【Tim】设法让这种支持发挥作用。

如果你想知道是否可以用公式而不是表格来计算 MIDI 音调的频率，答案是肯定的。使用 emscripten 可以轻松编译，但集成到 roll up . js——一个 JavaScript 框架——需要一点工作，您可以在帖子中找到这个过程。

如果你想了解更多关于 [WebAssembly](https://hackaday.com/2019/04/04/webassembly-what-is-it-and-why-should-you-care/) 的信息，请查看我们之前的帖子。我们以前也看到过[在网络上做一些有趣的事情。](https://hackaday.com/2020/08/30/olaf-lets-an-esp32-listen-to-the-music/)

 [https://www.youtube.com/embed/QJ0k_Qa5VGI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QJ0k_Qa5VGI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

