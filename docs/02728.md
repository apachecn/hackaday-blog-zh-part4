# 带有 E-Ink 显示的 GPS 自动调整时钟

> 原文：<https://hackaday.com/2019/04/24/gps-self-adjusting-clock-with-an-e-ink-display/>

如果你提到通过无线电接收时间的时钟，大多数人会想到从 WWVB、MSF 或 DCF77 等电台接收长波信号的时钟。然而，最近的一个趋势是时钟可以根据轨道导航卫星自动校准，一个来自[KK99] 的例子。这是一个相对简单的硬件构建，因为它只是一个 Arduino Nano、GPS 模块和电子墨水显示模块连接在一起，但它提供了一个有趣的练习来运行 GPS 时钟所需的代码。

然而，它确实给了我们一个机会来记住去年围绕 WWVB 的故事，因为去年的一项预算提案提出了关闭位于柯林斯堡的时间信号发射器的前景。如果发生这种情况，估计有 5000 万只美国时钟将失去它们的参考，尽管它们的主人总是可以手动更新它们，但总会有基于时间的系统因为任何原因而无法应用。与此同时，欧洲人的时间传输目前是安全的，但如果他们认为他们有电网可以依靠，那就值得记住[他们失去 6 秒的时间](https://hackaday.com/2018/03/09/europe-loses-six-minutes-due-to-sagging-frequency-and-international-politics/)。

GPS 卫星图片:美国空军[ [公共领域](https://commons.wikimedia.org/wiki/File:Navstar-2F.jpg)。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)