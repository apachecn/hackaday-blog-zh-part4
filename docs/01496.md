# 用批处理文件引导 MSDOS 汇编程序

> 原文：<https://hackaday.com/2018/12/10/bootstrapping-an-msdos-assembler-with-batch-files/>

你有一个干净的 MSDOS 系统，你需要为它写一些软件。你是做什么的？当然，您可以使用 debug。但是没有标签，所以虽然你可以从助记符中获得机器代码，但你仍然需要自己找出地址。这对[mniip]来说还不够好，他[主要使用批处理文件](https://github.com/mniip/BOOTSTRA)创建了一个汇编器。有几个。COM 文件，看起来好像是第一次使用 debug 来创建这些文件，但也有一些源代码可以在后续的编译中使用汇编程序进行汇编。

为什么？我们不完全确定。但绝对是黑客。这种技术让我们想起了我们自己的通用交叉汇编器。

有几件事使这个工作。第一，没有太多 8086 指令需要担心。其次，您必须使用一种特殊的格式——本质上是在操作码前加上 CALL。这使得汇编程序不必解析操作码。你实际上用指令的名字调用一个批处理文件。例如:

```
CALL PUSH CS
CALL POP DS
CALL MOV DX WORD %String%

CALL LABEL String
REM H e l l o , w
CALL DB 72 101 108 108 111 44 32 119
```

该代码片段显示了另一个细微差别。你必须调用 LABEL 来引入一个标签。要在指令中使用标签，必须用百分号将它括起来。

当然，实际上，您可以使用 [gcc](https://hackaday.com/2018/05/14/msdos-development-with-gcc/) 来构建一个合适的汇编器。但是这其中的运动在哪里呢？