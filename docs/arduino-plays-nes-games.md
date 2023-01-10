# Arduino 玩 NES 游戏

> 原文：<https://hackaday.com/2020/07/15/arduino-plays-nes-games/>

随着时间的推移，通过观察各种组件的改进规格，观察技术的进步已经足够有趣了。但是与过去相比，与现代技术的实际实现相比，时钟速度、内存大小和功耗都是相当无形的。例如，这款 40 美元的微控制器[可以做 80 年代视频游戏控制台](https://github.com/nathalis/NESDUE-Arduino_DUE_Nintendo_emulator)所能做的事情，价格仅为(通胀调整后)的十分之一。

NESDUE 是一个完全在 Arduino Due 上运行的 NES 游戏模拟器。不过，Arduino 确实有一些限制，必须解决这些限制才能让任天堂正常工作。首先，它需要超频才能玩，而且它还需要一个变通办法来突破 96 kB 内存的限制。从那里，一个小屏幕和一个控制器(来自超级任天堂)连接起来，游戏就可以开始了。

对于一个 Arduino 平台来说，这是一个令人印象深刻的壮举，尤其是在必须进行大量内存调整的情况下。这可能是目前最先进的游戏系统，可以在 Arduino 上运行一切，[就像 Arduinocade](https://hackaday.com/2015/09/17/retro-games-on-arduinocade-just-shouldnt-be-possible/) 一样，可以直接从 Arduino 上提供类似街机的体验。

 [https://www.youtube.com/embed/gQ0J5JybFUg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gQ0J5JybFUg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

