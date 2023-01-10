# 2020 年会是 Linux 内核生锈的一年吗？

> 原文：<https://hackaday.com/2020/07/15/will-2020-be-the-year-of-rust-in-the-linux-kernel/>

现代编程语言的一个问题是，由于互联网的存在，它们的过度热情的早期采用者如今拥有了影响力。因此，其他人第一次接触它们时，往往是一些粗糙的、狂热的尝试，用这种闪亮的新语言重写每个已建立的软件项目——只是因为——这可能会留下令人讨厌的味道。然而，Rust 现在似乎已经超越了这种状态，并且随着它在普通开发人员中日益流行，可以肯定地说它将会继续存在。有一天会完全取代 C 吗？可能不会，但是共存的机会很大，【尼克·德索尔涅斯】[已经在 Linux 内核](https://lore.kernel.org/lkml/CAKwvOdmuYc8rW_H4aQG4DsJzho=F+djd68fp7mzmBp3-wY--Uw@mail.gmail.com/T/)中开始着手此事。

现在，在你通过寻找一个新的操作系统来发誓效忠 C 之前:什么也没有发生。[Nick]简单地测试了 Linux 内核代码库内 Rust 的可能未来，这是他计划在今年的 Linux 管道工会议(一年一度的内核开发人员聚会)上提出来讨论的事情。有趣的部分是[Linus Torvalds]在 LKML 线程上的[回应](https://lkml.org/lkml/2020/7/10/1261)，这让每个人都希望有一个类似于[的 c++ one](http://harmful.cat-v.org/software/c++/linus)的衷心签名 Rust rant 失望了。相反，他主要担心的是，在构建系统中引入这种支持会隐藏可能的错误，因此如果 Rust 编译器存在，应该自动启用这种支持——本质上意味着他似乎另有打算。

我们会看到它会带来什么，但是随着 Rust 语言团队负责人[Josh Triplett]声明有益于和推进内核集成的增强对于 Rust 本身来说肯定是可以想象的，我们可能会在不久的将来看到有趣的合作。如果你不想等待，今天就在用户驱动中使用 Rust，[看看这个 35c3 的演讲](https://hackaday.com/2018/12/31/35c3-safe-and-secure-drivers-in-high-level-languages/)。如果这对你来说还不够的话，[这里有一个用 Rust](https://hackaday.com/2018/09/08/pun-intended-bare-metal-attracts-rust/) 编写的完整(非 Linux)内核。