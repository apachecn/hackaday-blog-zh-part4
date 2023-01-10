# 任天堂游戏&手表上的厄运

> 原文：<https://hackaday.com/2020/11/22/doom-running-on-the-nintendo-game-watch/>

今天新发布的[任天堂游戏&手表可以玩毁灭战士](https://www.youtube.com/watch?v=sNg_S9UM5ps)。当然，也有警告…由于硬件本身的限制，这是一个淡化的版本。但重要的是，这表明硬件已被完全拥有。这是用来替换 STM32 中的固件的代码，这使得这个华丽的小硬件平台对自制黑客完全开放。

老实说，考虑到投入的努力，你不得不假设这将很快发生。我们[首先在周二](https://hackaday.com/2020/11/17/exploring-the-new-super-mario-game-watch/)报道了存储游戏和手表 ROM 的 EEPROM 存储器已经被解码。在那篇文章发表后不久，[ [stacksmashing](https://twitter.com/ghidraninja) 和[ [Konrad Beckmann](https://twitter.com/kbeckmann) ]在显示器上显示测试模式，并提到音频也在工作。结果是尽管芯片被安全锁定了，他们还是能转储库存固件。

我们必须等待更多关于如何转储固件的细节，但[stacksmashing]在下面的视频中提到了足够多的内容来证实这一点。从锁定的微控制器转储代码的一种常见方法是找到一个允许执行自定义代码的漏洞。只需运行几行自己的代码，就足以设置一些简单的东西，比如遍历所有内部闪存地址，并通过几个 GPIO 引脚将它们转储。在这种情况下，我们的两个英雄发现一些 ARM 代码正在从 EEPROM 加载到 STM32 上，并设法注入他们自己的指令来执行转储。他们答应很快公布全部细节。

我们今天所拥有的是一个相当棘手的黑客技术，不仅仅是加载代码，而是让 DOOM 在微薄的硬件规格上运行。值得注意的是，128 k 的 SRAM 和 1.3 MB 的外部 RAM。存储游戏文件的 1.1 MB 闪存也是一个瓶颈。纹理被剥离下来，内存分配被重写，但概念证明在那里，游戏运行。家酿，我们来了！

 [https://www.youtube.com/embed/sNg_S9UM5ps?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sNg_S9UM5ps?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[感谢@arturo182]