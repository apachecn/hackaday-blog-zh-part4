# 通过 Forth 的网页

> 原文：<https://hackaday.com/2018/08/02/web-pages-via-forth/>

第四。你要么喜欢它，要么讨厌它。如果你一直在努力开发微型微控制器，你可能属于第一个阵营。毕竟，启动一个最小的 Forth 系统非常简单，只需要很少的 CPU 资源。一旦你有了这样的环境，就很容易向前扩展。[Remko]决定他想要建立一个第四代编译器，它使用 WebAssembly 并且[在你的浏览器](https://el-tramo.be/waforth/)中运行。为什么？我们学会了不要过多考虑这个问题。

自从 1990 年首次推出万维网浏览器以来，世界已经发生了很大的变化。最初是一种在网络上显示文本文档的方式，现在已经变成了一个应用平台，不管是好是坏。JavaScript 赢得了浏览器脚本语言的战争，而安全问题几乎扼杀了 Java 小程序和 Flash。但是 JavaScript 并不总是很快。当然，有一些方法可以实现即时编译，比如谷歌的 V8 引擎。但是编译步骤也需要时间。输入 WebAssembly(或 Wasm)。

就像 C 程序员为了提高性能可能用汇编语言编写代码的某些部分一样，JavaScript 开发人员也可以用 Wasm 构建速度关键的代码。Wasm 定义了一种文本格式和一种二进制格式，便于浏览器理解和执行。第四代编译器主要使用文本格式，并为一些函数使用一些 JavaScript。当然，很多也是在第四章写的。

如果你讨厌 Forth，你现在可能已经放弃阅读了。我们喜欢在 BluePill 上使用 [Forth，这是一个非常便宜的开发系统。我们以前也见过 JavaScript](https://hackaday.com/2017/08/04/take-the-blue-pill-and-go-forth/) 中的 [Forth。对 JavaScript 和 Wasm 版本进行基准测试，看看 Wasm 的表现会很有趣。](https://hackaday.com/2017/01/04/browsing-forth/)