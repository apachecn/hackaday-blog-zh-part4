# 自制的 CPU 使用自制的工具链运行

> 原文：<https://hackaday.com/2022/11/22/home-built-cpu-runs-with-home-built-toolchain/>

几年前,[高屋佐伯]和东京大学的同学们在他们的“CPU 练习”课上接受了非常有限的指导，大致如下:

> 用 OCaml 编写这个光线跟踪程序，在 FPGA 上实现的 CPU 上运行它

分成小组，涵盖 CPU、FPU、模拟器工具和编译器工具链，学生们从设计 RISC ISA 开始，然后围绕它设计 CPU。您可以跟随 [回顾](https://fuel.edby.coffee/posts/how-we-ported-xv6-os-to-a-home-built-cpu-with-a-home-built-c-compiler/) 类的文章，然后深入 GitHub 页面了解系统的每个组件，尽管评论主要是日语。嘿，你会谷歌翻译吧？

最初的任务是在 FPGA 托管的 CPU 上运行光线跟踪演示，但学生们走得更远，移植了 Xv6，这是一个用于教育用途的类 Unix 操作系统， [由麻省理工学院](https://github.com/mit-pdos/xv6-public) 提供，然后在此基础上运行 OCaml 光线跟踪演示。Xv6 是为 x86 设计的，而不是他们自己的 ISA，所以在编译器工具链上需要做大量的工作。显而易见的途径是移植 LLVM 或 GCC，但该小组决定从头开始制作他们的 C89 兼容工具链会更有趣，于是 [UCC](https://github.com/keiichiw/ucc) 诞生了！

[原来的 CPU](https://github.com/is-cpuex2014-5/core) 没有 MMU 或中断处理，所以这需要添加到设计和模拟器中。其中一个团队添加了支持类 Unix 操作系统所需的额外硬件功能，生产了一种 [新 CPU 设计，他们将其命名为 GAIA](https://github.com/nyuichi/GAIA3) 。Xv6 的最终版本为盖亚 CPU 可以在 [这里找到](https://github.com/nyuichi/xv6) 。如果你想玩玩这个，他们甚至制作了一个 Javascript 版本(使用 emscripten ),这样你就可以在你的浏览器中运行[](https://nullpo-head.github.io/emcc-gaia-simu/xv6.html)！啊呀，我们认为我们的学生项目很难，更不用说做 *这个* 来获得额外的学分了！

现在，我们知道你在想什么——头号问题——它能运行 doom 吗？我们还不知道，但在 Hackaday 上，总有 [另一个在拐角处，可以](https://hackaday.com/2022/08/16/recreating-doom-on-a-homebrew-8-bit-cpu/) 。