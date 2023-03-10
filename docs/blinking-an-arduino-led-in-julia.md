# Julia 的 Arduino 指示灯闪烁

> 原文：<https://hackaday.com/2022/06/20/blinking-an-arduino-led-in-julia/>

Julia 编程语言非常适合 ATMega328p 这样的简单微控制器，它位于经典的 Arduino 中，[但这并没有阻止【Sukera】的尝试和成功](https://seelengrab.github.io/articles/Running%20Julia%20baremetal%20on%20an%20Arduino/)。

所有让 Julia 成为你的大型计算机的酷编程语言的特性都让它成为 Arduino 的糟糕选择。它是为交互性而设计的，是动态类型的，并且严重依赖于它的垃圾收集；光是这些特征中的每一个都会让 Mega 的税收达到崩溃的边缘。但对它有利的是，它是一种基于 LLVM 的编译语言，LLVM 有一个用于 c 的 AVR 后端。应该只是一个简单的问题，去掉一些开销，重新编译 LLVM 以添加一个用于 Julia 的 AVR 目标，然后解决所有其他的遗留问题，对吗？

好吧，结果几乎是。严重依赖于 LLVM 的灵活性，[Sukera]设法关闭了所有不需要的语言特性，在遇到一些小障碍后，比如 volatile 和 atomic 变量的常见问题，设法让 LED 缓慢闪烁。万岁。我们喜欢 Sukera 的讽刺:“这就是我所说的两天过得很好！”在这一切都完成后，但说真的，这是我们第一次看到超级初级的 Julia 代码在 8 位微控制器上运行，所以这里肯定有一些荣誉。

当 Julia 进入 AVR 时，它在大型计算机上的许多吸引力在 micro 上消失了，所以我们真的没有看到人们选择它而不是拥有更发达生态系统的 straight C。但是，看到围绕运行时和垃圾收集设计的语言能够在我们最喜欢的微型计算机上运行，还是很棒的。

谢谢[Joel]的提示！