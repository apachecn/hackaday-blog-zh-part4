# 一个简单的指南来解锁任天堂游戏和手表

> 原文：<https://hackaday.com/2020/12/02/a-straightforward-guide-to-unlocking-the-nintendo-game-and-watch/>

任天堂重生的微型掌上游戏当然吸引了硬件黑客的注意，随着它的秘密一个接一个地被揭开，我们已经受到了一连串的攻击。凭借相对简单的硬件，它隐藏了远远超出一两个简单的 *Mario* 游戏的潜力，现在它已经可以转储 SPI 闪存和内部闪存，解锁处理器，并运行任意代码。[解锁的过程现在已经足够向前推进，足以保证一个 HOWTO 视频](https://www.youtube.com/watch?v=-MzmoEFs0bQ)，【stacksmashing】已经对我们进行了处理。现在还为时尚早，它仍然被吹捧为面向开发者而非游戏玩家，但它显示了这款游戏机的发展方向。

控制台的 STM32 架构意味着编程硬件很容易找到，尽管我们被警告不要使用廉价的全球速卖通类型，我们可能会使用蓝色药丸或类似的东西。相反，STM Nucleo 板附带的 snap-off 编程器是一个更安全的选择，许多人可能已经有了。

从下面的视频中可以看出，这一过程相对简单，但对多人来说却隐藏了大量的工作。它是一系列的脚本，为每一步顺序解锁和备份带有 STM 有效载荷的各种固件。最后，STM32 本身被解锁，备份的任天堂固件可以返回到设备上，或者创建一个定制的固件。除了[我们已经看到的厄运](https://hackaday.com/2020/11/22/doom-running-on-the-nintendo-game-watch/)之外，还有正在开发中的 NES 和 Game Boy 模拟器，令人着迷的是它们也在裸机游戏上工作。

鉴于这款游戏机缺乏定制芯片，它的硬件很可能被直接克隆，任天堂可能无意中创造了一个新的通用黑客手持游戏平台。有一些硬件工作正在进行中，如增加 SPI 闪存大小和找到未连接的 USB 引脚，因此我们期待本季度更多令人兴奋的消息。

 [https://www.youtube.com/embed/-MzmoEFs0bQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-MzmoEFs0bQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

