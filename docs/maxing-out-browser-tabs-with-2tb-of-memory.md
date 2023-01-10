# 2TB 内存最大化浏览器标签

> 原文：<https://hackaday.com/2020/03/30/maxing-out-browser-tabs-with-2tb-of-memory/>

标签式浏览改变了游戏规则，允许用户有效地同时浏览多个网站，而不会丢失上下文。事实证明，这是一个比使用多个窗口更好的解决方案，也是一个受到所有人称赞的效率优势。我们中的许多人都是标签迷，一次打开大量的数字是我们工作流程中的习惯性部分。[Linus]决定弄清楚在配备了 2TB 内存的系统上他能打开多少个。

显而易见，建立一个 2TB 内存的系统绝非易事。采购了特殊的服务器级 RAM 模块，每个模块封装 128 GB RAM，用于 ECC 操作。打包 16 个插槽，用单个 CPU 处理这么多 RAM 会有性能损失，但对于内存密集型工作来说，这是值得的。问题中的 CPU 是 AMD 64 核处理器，为手头的任务提供了大量的工作量。

在测试中，机器在内存满之前很久就开始减速。超过 5000 个标签，事情开始慢慢发展。在 6000 个标签中，打开更多的标签是不切实际的，机器需要整整 26 秒来响应一次点击。此时的内存使用量只有 200GB，这表明软件的限制阻碍了打开更多的标签页。

虽然这不是衡量任何重要事物的有用标准，但是探索极限还是很有趣的。我们以前见过他们的项目，比如这个原始的 Xbox casemod。休息后的视频。

 [https://www.youtube.com/embed/7iwgyzX-76g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7iwgyzX-76g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

