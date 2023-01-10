# 程序生成的反计算机模拟器

> 原文：<https://hackaday.com/2020/11/06/procedurally-generated-retrocomputer-emulators/>

【极客侯爵】对旧系统有着深厚的热爱。厌倦了为每个项目从头开始编写新的模拟器，[他的最新项目 EMF 为他生成模拟器](http://em.ulat.es/info.php)。XML 文档描述了内存布局、CPU 描述和屏幕处理程序。目前的输出是一个带有汇编器和反汇编器的单页 Javascript 模拟器应用程序。然而，后端可以很容易地转换成另一种语言，如 Rust 或 C++。

因为 EMF 是一个框架，它提供了一种描述仿真机器的通用方法，所以您可以免费获得一个通用的仿真器用户界面。这里也提供了很大的灵活性。根据目标语言的性能，操作码可以实现为一个大的 switch 语句或单独的函数。可以单独检测和处理自修改代码。通过用目标语言编写一个模块，可以很容易地注入定制的特性或硬件。

虽然 EMF 的源代码尚未发布，但[极客侯爵]用 EMF [建造的几台机器在 GitHub](https://github.com/MarquisdeGeek) 上是开源的。到目前为止，该列表包括 Dragon32、Sinclair ZX80、Sinclair ZX81、Sinclair ZX Spectrum、Elliott 903、Chip8、Cosmac VIP 和 MegaProcessor。每个都有一个运行在浏览器中的实时仿真器。

虽然[极客侯爵]希望很快发布 EMF 的二进制版本，但我们非常期待一旦代码清理完毕，EMF 源代码就会出来。我们喜欢创建更容易和更容易使用的模拟器的趋势，比如运行 Atari 程序的 Twitter 机器人。

 [https://www.youtube.com/embed/S1yKaqZfOSM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S1yKaqZfOSM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Steven]发送这封邮件！