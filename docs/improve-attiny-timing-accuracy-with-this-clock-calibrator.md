# 使用此时钟校准器提高 ATtiny 计时精度

> 原文：<https://hackaday.com/2020/12/30/improve-attiny-timing-accuracy-with-this-clock-calibrator/>

较小的 ATtiny 微控制器引脚数量有限，因此依赖内部 9.6 MHz 振荡器，而不是外部晶体。这种振荡器缺乏晶振的精度，因此单个芯片可能与标称值相差很大。令人高兴的是，由此产生的计时误差可以通过校准过程来缓解，Stefan Wagner 已经将这一点纳入了他的微型校准器 T1 中。此外，它还具有所需的电荷泵电路，可以重置内部保险丝，以挽救“瘫痪”的态度，从而挽救那些小错误。

该板有自己的较大 attini，带有一个晶体振荡器和一个有机发光二极管屏，允许它测量测试 attini，并产生一个应用于芯片的校正系数。重复这个过程，直到与标准有最小可能的差异。你可以在 EasyEDA 上找到硬件的文件[，在 GitHub 仓库](https://easyeda.com/wagiminator/attiny84-tinycalibrator)中找到软件的文件[。](https://github.com/wagiminator/ATtiny84-TinyCalibrator)

很重要的一点是，结果永远不会像水晶一样稳定，所以建议你不要太相信这些计时器，但至少它们不会像发货时那样离谱。总而言之，如果你正在开发更小的 ATtiny 芯片，这是一个方便的板。

追求时钟准确性时要小心——它可能会让你掉进兔子洞。