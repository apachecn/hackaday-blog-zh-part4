# 猫砂和坏掉的灯泡为这台自制的气相色谱仪提供动力

> 原文：<https://hackaday.com/2019/08/08/kitty-litter-and-broken-light-bulbs-power-this-homebrew-gas-chromatogram/>

在 Hackaday，我们总是在寻找意想不到的预算，偶然发现一个售价数万美元的低成本 DIY 版本的乐器总是一种享受。因此，当我们今天早上在提示栏里看到一个自制气相色谱仪的提示时，我们就欣然接受了。(视频嵌入下方。)

对于那些没有享受过这种乐趣的人来说，气相色谱是一种化学分析方法，它能够将挥发性样品分解成其组成部分。像所有色谱方法一样，它使用固定基质来不同程度地延迟含有待研究样品的流动相的流动，从而可以测量通过系统的传输时间，并推断出样品的物理性质信息。

[Chromatogiraffery]建造的气相色谱仪使用一根长长的不锈钢管，管中充满了磨细的膨润土，通常被称为猫砂，作为固定相。挥发性样品与惰性载气(在本例中是来自派对气球罐的氦气)一起注入，并通过气压沿着猫砂柱传输。随着样品柱的移动，样品与柱相互作用，较大的物质被阻挡，而较小的物质则加速前进。使用热导池进行检测，热导池使用旧的白炽灯，这些白炽灯已经裂开，使其灯丝暴露在气流中；使用[惠斯通电桥](https://hackaday.com/2016/11/08/crossing-wheatstone-bridges/)和[差动放大器](https://hackaday.com/2018/11/13/whats-the-difference-ask-an-op-amp/)，通过 Arduino 读取并绘制纯载气和柱洗出液之间的温差。

家酿 GC 工作得出奇的好，我们已经等不及[Chromatogiraffery]公布他的构建的更多细节了。

 [https://www.youtube.com/embed/vc6VKQSX5j8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vc6VKQSX5j8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[叶禾]的提示。