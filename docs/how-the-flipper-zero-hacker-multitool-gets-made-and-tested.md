# Flipper Zero Hacker 多功能工具是如何制作和测试的

> 原文：<https://hackaday.com/2021/07/24/how-the-flipper-zero-hacker-multitool-gets-made-and-tested/>

*Flipper Zero* 是一款面向黑客的开源多功能工具，【Pavel】最近分享了[关于这些设备的生产和测试的细节](https://blog.flipperzero.one/electronics-testing/)。每个单元包含四个独立的 PCB，在大批量生产中，不可避免地会有一些电路板在某些方面出现故障。并非所有的错误都是相同的——有些甚至不明显——但它们都必须在最终成为成品之前得到处理。

[![](img/3b91374edc6c2e1cf3aa31543342df69.png)](https://hackaday.com/wp-content/uploads/2021/07/Flipper-Zero-test-jig.jpg)

One of several custom test jigs for Flipper Zero. Faults in high volume production are inevitable, and detecting them early is best.

设计有效检测和处理故障的流程是一项艰巨的任务，Flipper Zero 团队通过为每个独立的 PCB 设计独立的测试站来解决这一问题，从而尽可能早地检测出缺陷。每块板都被安装到一个定制的测试夹具中，然后接受一系列自动测试，以确保一切都符合预期，然后才会被批准。最终测试站对完成的组件进行检查，并且每个测试都被记录到数据库中。

跳过对单个电路板的测试，而是对完成的单元进行一次全面的测试，这看起来很诱人，但在处理生产错误时，尽可能早地在工作流程中发现问题是很重要的。问题发现得越晚，解决起来就越困难，成本也越高。最糟糕的结果可能是将有缺陷的部件交到客户手中，而只有在花费了组装和运输的所有时间和成本之后，才发现问题。尽早发现问题的另一个原因是，有些故障发现得越晚，解决起来就越困难。例如，当在完全组装的单元中检测到暗淡的 LED 或较差的天线性能时，很难排除故障，因为故障可能在任何地方。

[Pavel]提供了大量关于 Flipper Zero 制作的图片和细节，很高兴看到该项目自其超级成功的众筹活动以来的进展[。](https://hackaday.com/2020/09/02/flipper-zero-blasts-past-funding-goal-and-into-our-hearts/)