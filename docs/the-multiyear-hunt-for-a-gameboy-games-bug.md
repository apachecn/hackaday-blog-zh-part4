# 对 Gameboy 游戏漏洞的多年搜寻

> 原文：<https://hackaday.com/2020/01/31/the-multiyear-hunt-for-a-gameboy-games-bug/>

[Enddrift]在试图将经典游戏《Hello Kitty Collection:奇迹时尚制造者》运行到 GBA (Gameboy Advance)模拟器中时遇到了真正的问题。在启动过程中，游戏会遇到一个无限循环，等待从不存在的内存位置读取数据，因此不会在模拟器下启动。问题是，[游戏可以在真实的硬件上运行，即使内存也不存在于](https://mgba.io/2020/01/25/infinite-loop-holy-grail/)中。

更复杂的是，在 Sonic Pinball Party 下加载保存的游戏时，也存在类似的错误。然后一个口袋妖怪翡翠黑客浮出水面，帮助打破了案件。这个故事很有趣。

你可以在原始帖子中阅读详细信息，但结果是，读取 GBA 上的无效地址只是读取开放总线，因为该设备没有内存管理单元来抛出页面错误，即所谓的数据中止。结果是，您会期望一个开放的总线读取您读取或写入的最后一个值——一些数据或最后一次取指令。但事实远比这复杂。

代码不是从最后一次 CPU 内存读写中读取鬼值，而是从最后一次 DMA 周期中读取鬼值！这种变通方法也很聪明，因为它将预期的 DMA 结束时间与当前指令进行比较，并强制它读取正确的值。

一部伟大的侦探作品。我们不确定我们是不是在排队玩凯蒂猫，但很高兴知道我们可以。尤其是如果我们的真实设备中有一个仿真器[。如果你的黑客欲望更多的运行到真实的硬件，我们会建议](https://hackaday.com/2016/11/03/emulating-a-gameboy-advance-inside-of-a-gameboy-advance/)[这个 FPGA 项目](https://hackaday.com/2019/02/21/fpga-brings-arduboy-to-the-game-boy-advance/)。