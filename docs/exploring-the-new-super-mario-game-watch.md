# 探索新的超级马里奥游戏&观看

> 原文：<https://hackaday.com/2020/11/17/exploring-the-new-super-mario-game-watch/>

任天堂已经恢复了经典的*游戏&手表*，这一次是光荣的全彩色，运行的是 1985 年首次出现在任天堂娱乐系统(NES)的*超级马里奥兄弟*。尽管它才上市几天，[stack mashing]已经在释放这款 50 美元复古手持设备的全部潜力方面取得了一些令人印象深刻的进展[。](https://github.com/ghidraninja/game-and-watch-hacking)

对于一般的黑客读者来说，我们在这里看到的是一个口袋大小的 NES 仿真器是不足为奇的，但是在[stacksmashing]打开它之前，没有人能够确定它运行的是哪种硬件。令人欣慰的是，没有一个环氧树脂滴在视线中，所有的芯片都很容易识别。了解到*游戏&手表*运行在 STM32H7B0 微控制器上，附近有一个保存固件的 SPI 闪存芯片，这只是弄清楚软件如何工作的问题。

[![](img/ec215703e1895f575d4e01ecac5d55d8.png)](https://hackaday.com/wp-content/uploads/2020/11/newgw_detail1.jpg)

Connecting to the SWD header.

没过多久，他就发现电路板上的一个[未填充接头可以让他访问 STM32 的串行线调试(SWD)](https://hackaday.com/2020/02/11/xbox-controller-provides-intro-to-swd-hacking/) 接口，尽管不幸的是，他发现芯片的安全模式已启用，他无法转储固件。

但他能够通过 SWD 转储内存，这使他能够识别超级马里奥兄弟 NES ROM 住在哪里。通过将 SPI 闪存芯片连接到读卡器，并将其内容与系统 RAM 中的内容进行比较，[stacksmashing]能够找出 XOR 加密方案，并推出一种工具，允许您将修改后的 ROM 插入到可以成功闪存到芯片的映像中。

这是不是意味着你可以把任何你想要的 NES ROM 放到新的*游戏&手表*上？不幸的是，我们还没到那一步。运行在设备上的模拟器有一些奇怪的地方，在它准备好运行*魂斗罗*之前，还需要一些额外的哄骗。但是[我们已经看够了这些设备被黑](https://hackaday.com/2019/12/06/swapping-the-roms-in-mini-arcade-cabinets/)知道这只是时间问题。

 [https://www.youtube.com/embed/Rsi8p5gbaps?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Rsi8p5gbaps?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 NeoTechni 的提示。]