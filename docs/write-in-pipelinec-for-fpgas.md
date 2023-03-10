# 写入 FPGAs 的 PipelineC

> 原文：<https://hackaday.com/2020/08/16/write-in-pipelinec-for-fpgas/>

当您有一个大规模并行应用时，现场可编程门阵列(FPGAs)的最大好处是一切都可以并行运行。当你需要一大堆事情按顺序发生时，FPGAs 最糟糕的一点就是一切都是并行运行的。例如，如果你有一个多步骤的计算，你需要把它分成几个块，找出它们之间的时间，并确保每个块在被输入新数据之前都被清空。这就是流水线操作，自己处理所有底层细节是有时可以让 FPGA 成为以“F”开头的四个字母单词的事情之一。

[Julian kemmer]的 [PipelineC](https://github.com/JulianKemmerer/PipelineC) 是一种类似 C 的语言，它可以编译成 VHDL，这样你就可以在 FPGA 中使用它，它会为你完成流水线操作。他举例说明了如何用它来[构建一个简单的状态机](https://github.com/JulianKemmerer/PipelineC/wiki)，并且在你写了几百个状态机之后，你会知道为什么这是一个好主意。

PipelineC [不是唯一的高级合成语言](https://hackaday.com/2019/10/28/chisel-away-at-fpga-development/)，但是它有一个有趣的地方。它不负责内存或定义接口。它只负责流水线操作。我们还没有尝试过，但它看起来对中等复杂的项目会很有趣，在这些项目中,[管道信号](https://zipcpu.com/blog/2017/08/14/strategies-for-pipelining.html)的机制是一个麻烦，但你不需要豪华的待遇。检查一下，如果你喜欢，让我们(和(朱利安)，当然)知道。

如果你想一头扎进流水线，看看两集迷你剧。

管道图[CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/)BY[CBurnett](https://en.wikipedia.org/wiki/User:Cburnett/GFDL_images#/media/File:Pipeline,_4_stage.svg)