# TinyGo 为 Arduino 带来围棋

> 原文：<https://hackaday.com/2019/09/04/tinygo-brings-go-to-arduino/>

起源于 Google 的现代编程语言 Go 是有望取代 C(和 C++)成为传统编程语言的新一代语言之一。不过，这只适用于个人电脑，对吗？没那么快！TinyGo 提供了一个编译器——用他们的话说——是为小地方准备的。有多小？他们可以瞄准 Arduino Uno 或 BBC micro:bit 的代码。它还可以为 x86 或 ARM Linux(32 位和 64 位)以及 WebAssembly 生成代码。他们声称，最近一个为 LLVM 添加 ESP8266 和 EPS32 支持的项目最终将使 TinyGo 也能够针对这些平台。

正如你所料，TinyGo 和成熟版本之间有一些细微的差别。编译器一次处理整个程序，速度较慢，但提供了更多的优化。TinyGo 中没有使用对接口方法的某些优化，全局变量处理发生了变化，以适应高效地将数据从闪存移动到 RAM。TinyGo 在寄存器中传递参数。

其他的变化更加深刻。例如，还没有垃圾收集，所以在初始化之后不要执行堆分配。还有一些其他主要功能不受支持。goroutines 和 channels、cgo、反射和三个索引片形式的并发是行不通的。地图是可用的，但是只有某些关键类型。由于缺失的部分，标准库中的许多包都无法构建。

当然，处于相同位置的另一种现代语言是 Rust，如果你想知道为什么用 Go 而不是 Rust，这里有一个 [FAQ](https://tinygo.org/faq/why-go-instead-of-rust/) 来回答这个问题。你需要去 Arduino 吗？也许不是。然而，如果你是一个围棋程序员，也许这为你打开了一些可能性。

我们记得有个[黑客点唱机用了 Go](https://hackaday.com/2017/06/02/hackerspace-jukebox/) 。我们还记得有人在命运多舛的[英特尔爱迪生](https://hackaday.com/2014/09/25/running-golang-on-the-intel-edison/)上使用了它。