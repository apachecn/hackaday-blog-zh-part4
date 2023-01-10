# 新出炉的 Javascript 运行时

> 原文：<https://hackaday.com/2022/07/08/a-new-javascript-runtime-fresh-out-of-the-oven/>

当一些新奇的 Javascript 东西出现时，相当一部分黑客观众会抱怨并流眼泪。那么是什么让 Bun 与众不同呢？ [Bun 是一个运行时(像 Node 或 Deno)](https://bun.sh/) t，它提供了一个高性能的一体化方法。让辣妹高兴的是，这是用齐格语写的[。它提供捆绑、传输、模块解析和一个奇妙的外部函数接口。](https://hackaday.com/2021/10/05/need-a-new-programming-language-try-zig/)

Node.js 和 Deno 运行在 V8 Javascript 引擎上，并提供 Node-API 来访问不同的特性，例如不适用于 web 浏览器的文件系统。然而，围绕 Node.js 和 NPM(节点包管理器)已经建立了大量的工具。许多 Javascript 项目都有一个打包和传输步骤，将源代码以更标准的格式打包在一起。Typescript 需要打包成 javascript，模块需要解析。

Bun 把这些都烤进去了。打字稿和 JSX“只是工作。”这极大地简化了许多项目，因为许多构建基础设施是 Bun 本身的一部分，降低了试图理解项目时的认知负荷。SQL 客户端和 Jest 式单元测试运行器都是内置的。而不是 V8，它使用 JavaScriptCore，启动速度稍快。但是 Bun 提供的令人难以置信的加速主要来自于它是用 Zig 编写的，以及致力于基准测试、剖析和优化的巨大努力。更疯狂的是，Bun 是一个人写的，Jared Sumner。

由于 Bun 实现了大多数节点 API(以后还会有更多)，许多模块都是插件兼容的。一些特定于 web 的 API，如 fetch 和 Websockets，也是内置的。这是一个早期项目，我们对项目开发者的任何声明都持怀疑态度，但我们持谨慎乐观的态度。即使你不擅长 Javascript，你也可能最终会学习 WebAssembly。[Fireship]的一个短视频很好的概述了这一点。[如果你想自己看的话，Bun 的所有代码都在 Github](https://github.com/Jarred-Sumner/bun) 上，有麻省理工学院的许可。

感谢[迈克尔·卡尔森]给我们讲了这个可怕的辣妹笑话。

 [https://www.youtube.com/embed/FMhScnY0dME?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FMhScnY0dME?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

