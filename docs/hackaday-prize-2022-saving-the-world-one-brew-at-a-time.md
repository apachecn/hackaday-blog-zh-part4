# 2022 年 Hackaday 奖:拯救世界，每次一杯啤酒

> 原文：<https://hackaday.com/2022/08/05/hackaday-prize-2022-saving-the-world-one-brew-at-a-time/>

好吧，也许[撒旦主义者]在他的项目标题“[拯救咖啡，拯救世界](https://hackaday.io/project/186490-save-the-coffee-save-the-world)”上做得有些过火，但通过破解其损坏的显示屏，让一台正常工作的咖啡机远离垃圾填埋场，仍然是一项值得追求的目标。汁液必须流动！

被破坏的显示器使用了 SSD1303 控制器 OLED 模块，SSD1305Z 是几乎兼容的模块。差不多了。一个小问题是默认情况下屏幕是反方向填充的。翻遍手册，有一个屏幕方向位要设置，用逻辑分析仪追踪通信，每次屏幕刷新都设置错误。要是他能在运输过程中稍微翻转一下就好了。是时候做中间人了！

虽然我们肯定会在游戏中加入微控制器，但[撒旦崇拜]还是老派了。双 IC 逻辑解决方案可以做完全相同的事情，用电线换代码。转换器板的最后一次迭代相对简单，但它完成了一项工作。

因此，如果您有一台显示不清晰的 Nivona 咖啡机，或者安捷伦 U1273A 万用表，或者任何其他需要难以找到的 SSD1303 控制器的设备，现在您就有了现成的解决方案。但如果没有，你发现自己正在寻找一个你找不到的展示，让这个作为你的一个例子——用一点点(有趣的)努力，你可以把它黑回来。

The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)