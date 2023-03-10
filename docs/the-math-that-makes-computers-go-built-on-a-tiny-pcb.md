# 让计算机运行的数学，建立在一个小小的印刷电路板上

> 原文：<https://hackaday.com/2018/10/18/the-math-that-makes-computers-go-built-on-a-tiny-pcb/>

从本质上讲，计算机只是一堆连接在一起的晶体管。一旦你在一块板上有了足够多的晶体管，首先出现的抽象层之一就是算术逻辑单元。ALU 接收两组数据，执行选定的数学函数，并输出一组数据作为结果。这真的是计算机计算的核心。

现代处理器中内置了 ALU，但这并不总是如此。如果你想再造一台早期的计算机，你可能需要一台独立的，这就是为什么[roelh]使用五个多路复用器芯片和两个 XOR 芯片设计了一个适合一平方英寸电路板的[ALU。](https://hackaday.io/project/160506-4-bit-ttl-alu)

用于此目的的常用组件之一 [74LS181 ALU](https://hackaday.com/2017/03/27/explaining-the-operation-of-the-74181-alu/) 已经停产。[roelh 的] ALU 旨在成为各种小尺寸的替代品，可以执行七种功能:加、除、异或、XNOR、与、或、A、B 和 NOT A。小尺寸的设计是我们最近竞赛的一个限制:[方寸项目的回归](http://hackaday.com/?p=329249)。当然，这意味着额外的设计挑战，例如需要将进位和进位线移到单独的收割台，因为一边没有足够的空间。

探索 ALU 背后的理论不仅仅是为了建造逆向计算机的人。这对于获得对所有计算机如何工作的直观理解是不可或缺的。每个人都应该考虑通过浏览[NAND 2 Tetris 课程](https://hackaday.com/2012/10/11/programming-tetris-by-first-building-a-logic-gate-then-a-computer-then/)来了解内幕，该课程基于*计算科学*教科书的内容，使用模拟从与非门一直构建到正常工作的计算机。

如果你是一个自制计算机的制造者，使用这些 alu 中的一个可能比自己设计更值得。当然，如果[从零开始构建组件](https://hackaday.com/2011/02/25/building-a-555-timer-from-discrete-components/)是你的事情，我们当然也理解你的动机。