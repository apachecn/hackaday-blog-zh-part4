# Bixel，一种开源的 16×16 交互式 LED 阵列

> 原文：<https://hackaday.com/2018/09/12/bixel-an-open-source-16x16-interactive-led-array/>

Maniacal Labs 的[Adam Haile]和[Dan Ternes]显然没有忘记“要么做大，要么回家”这句话。多年来，他们一直在考虑创造一个巨大的 LED 矩阵，其中每个“像素”都是一个物理按钮。既然他们已经积累了其他 LED 项目的工作经验，他们最终决定是时候冒险创造他们的杰作:Bixel。

[![](img/015e0da1982d8ce3bff8828caa850829.png)](https://hackaday.com/wp-content/uploads/2018/09/bixel_detail.jpg) 创造 Bixel(按钮和像素的组合)绝非易事。[除了休息后的延时视频之外，这一史诗般的建造在车队网站](https://maniacallabs.com/2018/09/10/button-pixel--bixel/)上有特别详细的记录。[Adam]告诉我们 Bixel 花了大约 100 个小时组装，我们对此毫不怀疑。这确实是不太可能被复制的爱的劳动之一，尽管所有硬件和软件的源文件都是可用的，如果你足够勇敢的话。

这篇报道包含了许多关于 Bixel 设计和构造的迷人细节，但也许最不令人惊讶的是，最终产品与他们最初的设想大相径庭。计划是在 16×16 的网格中简单地使用发光的拱廊按钮，因为它们是专门为这些人的想法而建造的。但是当他们定价时，他们最多只能卖 2 美元一瓶。光是按钮*和*就要 500 美元，甚至在它们进入外壳或电子设备之前。像任何优秀的黑客一样，[亚当]和[丹]决定放弃现成的解决方案，想出自己的东西。

最后，他们从 RGB 条中切割出单个的 led，并将其焊接到定制设计的 500 毫米×500 毫米 PCB 上。每一部分的边上都有两个触摸开关，上面是一个由激光切割丙烯酸制成的“三明治”。最靠近 led 的板有一个 25 毫米的孔，最上面的板有一个 20 毫米的孔，在它们之间是一圈丙烯酸树脂，充当“按钮”。一旦全部拧在一起，按钮就不会从前面掉出来，也不会左右移动，但可以按下来接触触觉开关。

为了连接起来，他们[从 DIY 键盘场景](https://hackaday.com/2018/06/28/sunny-custom-keyboard-illuminates-the-past/)中得到启示，使用了一个小键盘、大约 595 个移位寄存器和 256 个 1N4148 二极管。运行 Python 框架的 Raspberry Pi 完成了繁重的计算工作，让 Teensy 只处理与硬件的对话。总的来说，如果你想以低廉的价格创建大量的按钮，这是一个很好的设计。比如[，只要你有时间去建造那个星际飞船模拟器](https://hackaday.com/2018/09/03/unleash-your-inner-starship-captain-with-this-immersive-simulator-console/)。

 [https://www.youtube.com/embed/scY-PhBbaS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/scY-PhBbaS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

