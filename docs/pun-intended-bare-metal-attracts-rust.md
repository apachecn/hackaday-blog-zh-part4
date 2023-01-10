# 双关语:裸露的金属会生锈

> 原文：<https://hackaday.com/2018/09/08/pun-intended-bare-metal-attracts-rust/>

编程语言往往会两极分化，Rust 到目前为止也不例外。它是否会继续存在并成长为较低层次的替代者——时间会证明一切。与此同时，如果你自己对这种语言及其底层能力感到好奇，[phil-opp]已经写了一系列关于在 Rust 中构建自己的小型裸机内核的博文。

从基础开始，[phil-opp]详细描述了创建独立可执行文件的设置和构建过程，该文件不会与 Rust 标准库相链接。从这里开始，他着手构建一个简单的操作系统内核，通过 VGA 输出打印一个不错的老式 Hello World 包括 QEMU 仿真。当然，还有一个包含所有源代码的 [GitHub 库](https://github.com/phil-opp/blog_os)。

[phil-opp]已经为此工作了一段时间，目前他正在编写该系列的第二版。因此，有些内容仍然缺失，但你可能会在他的第一版中找到更多。如果你一开始对铁锈一无所知，让我们后退一步[从基础开始](https://hackaday.com/2015/12/18/programming-with-rust/)。毕竟，[未来我们可能会看到更多。](https://hackaday.com/2018/03/12/baremetal-rust-on-the-horizon/)