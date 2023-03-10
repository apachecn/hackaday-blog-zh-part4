# 一台 Z80 自制游戏机，有一点现代的帮助

> 原文：<https://hackaday.com/2019/03/24/a-z80-homebrew-console-with-a-bit-of-modern-help/>

我们在 Hackaday 看到了许多逆向计算项目，这些项目采用 8 位时代的设备，并在 21 世纪重新创建它们。有时，它们保持准确的时间，并坚持所有当代设备，但在其他情况下，它们充分利用了四十年的先进技术。[【p killer】的 Z80 控制台](https://internalregister.github.io/2019/03/14/Homebrew-Console.html)就是后一类中的一种，它使用微控制器为经典 CPU 创建外围设备，取代了可能会在 20 世纪 80 年代的机器上出现的 74 逻辑或 ULA 芯片库。

视频生成硬件使用一种有趣的技术产生 PAL 信号，这种技术涉及两个 RAM 缓冲器。ATmega644 微控制器将单帧合成到一个缓冲器中，而另一个 ATmega644 从另一个缓冲器中生成前一帧视频。每次帧改变时，缓冲器在两个微控制器之间切换，需要一些额外的 74 逻辑芯片。另一个 AtMega 芯片为 Z80 提供了 I/O 接口，声音来自另一个双缓冲微控制器设置，并通过 YM3438 FM 合成芯片快速返回到经典硬件。结果可以在下面的视频中看到，在 80 年代末甚至 90 年代初的客厅里看起来都不会不合适。

有些人可能会问，为什么要费这么大的劲去追求这样一个项目，但这样做是没有抓住重点。当然，世嘉主系统可以从通常的来源，但在创建这样一个项目的建设者必须真正了解技术，如 PAL 代或 Z80 的内部细节。结果虽然不可否认地令人印象深刻，但与达到它的过程相比，几乎是次要的。

 [https://www.youtube.com/embed/2Pcrg1fesBk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2Pcrg1fesBk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Via [黑客新闻](https://news.ycombinator.com/item?id=19393279)，感谢【亚当·慕尼黑】的提示。