# Remoticon 2021 // Matt Venn 帮你做 ASICS

> 原文：<https://hackaday.com/2022/02/17/remoticon-2021-matt-venn-helps-you-make-asics/>

如果在 130 纳米工艺的硅片上给你 10 平方毫米的空间，你会做什么？这正是开放 MPW 项目提出的问题，[马特·文]站出来回答了这个问题。[Matt]在 2020 年来到 [Remoticon，讲述他从一无所有到自己的 ASIC，](https://hackaday.com/2020/12/29/remoticon-video-from-zero-to-asic-how-to-design-in-silicon/)的旅程，他在 2021 年回来，讲述一年来发生的事情。

[![image of the metal layers of an IC](img/6e381d2849a8120d9c057d5c985d9c77.png)](https://hackaday.com/wp-content/uploads/2022/02/maxB.png)

【maxi borga】一直在[为他和其他人的芯片设计制作精美的渲染图](https://twitter.com/maxiborga/)

我们期待伟大的设计，但我们认为提交的各种令人兴奋和精彩的设计超出了我们的预期。【Matt】经历了相当多的，比如一个[模拟神经元](https://efabless.com/projects/204)，一个 [RISC-V Arduino 兼容微处理器](https://efabless.com/projects/385)，一个[卫星收发器。也许艺术作品带来了意想不到的副作用。由于这些设计不在 NDA 奖之下，任何人都可以拿走这些设计并将其改造成华丽的东西。](https://www.zerotoasiccourse.com/post/interview-with-thomas-parry/)

当然，没有开放的工具链，所有这些硬件设计都是不可能的。有一种称为 OpenRAM 的 SRAM 生成器，可以为您的设计生成 RAM 模块。Coriolis2 是一个 RTL 到 GDS 的工具，可以在 VLSI 中进行布局和布线。最后，FlexCell 是一个单元库，它试图以灵活、可定制的方式提供标准功能，从而降低布局的复杂性。有一些 GitHub 动作可以在 PRs 上运行测试和仿真，以保持芯片的 HDL 处于良好状态。

然而，这并不是一帆风顺的，在第一次运行时(MPW1)出现了一个错误。未检测到违反保持时间的情况，并且时钟树不正确。这意味着 GPIO 不能被设置，所以中间的设计可以工作，但是没有 GPIO，很难确定。对于普通的芯片来说，这将是结束，但由于[Matt]可以访问布局和设计，他可以识别问题并提出计划。他计划用一个辅助微控制器来覆盖 IO 设置移位寄存器。(编者注:[tnt]最近取得了一些重大进展，[在本视频](https://www.youtube.com/watch?v=f_G5ad8SbHo)中进行了总结。)

看到这个项目到目前为止所取得的成果是令人难以置信的，我们期待着未来的运行。如果这让你相信你需要自己制作 ASIC，你应该看看[Matt]的"[零到 ASIC](https://zerotoasiccourse.com/) "课程。

 [https://www.youtube.com/embed/iK2yGvFety4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iK2yGvFety4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

