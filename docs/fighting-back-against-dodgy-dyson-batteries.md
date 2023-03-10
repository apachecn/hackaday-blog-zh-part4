# 反击狡猾的戴森电池

> 原文：<https://hackaday.com/2022/05/23/fighting-back-against-dodgy-dyson-batteries/>

如果你曾经使用过多节可充电电池组，你就会知道单节电池最终会变得不平衡。为了让电池组保持最佳工作状态，每个电池都需要单独分析和充电，这就是 RC 型电池组配备专用平衡连接器的原因。所以如果你知道，我们也知道，为什么戴森不知道？

正是这个问题激发了[【tin fever】开始从事 FU-Dyson-BMS 项目](https://github.com/tinfever/FU-Dyson-BMS)。正如你可能从名字中猜测的那样，[tinfever]认为戴森故意设计他们的 V6 和 V7 电池，不使用板载 ISL94208 电池管理 IC 的电池平衡功能。更糟糕的是，一旦电池失去平衡，哪怕只有 300 毫伏，控制器都会认为整个电池组都要报废，不再允许充电。

[![](img/66ecf6af0057718e0412cc57e5b7e0cc.png)](https://hackaday.com/wp-content/uploads/2022/05/fudyson_detail.png)

These missing resistors deserve justice.

或者至少，过去是这样的。随着替代固件[tinfever]的开发，电池组的电池管理系统(BMS)将忽略不平衡的电池，因此您可以继续使用电池组(尽管容量有所减少)。当然，理想的解决方案应该是在 ISL94208 上实现电池平衡，但不幸的是，Dyson 没有在 PCB 上包括必要的电阻。尽管值得注意的是，早期版本的电路板*确实有*未被占用的位置，这让戴森故意忽略这些位置的想法更加可信。

但并不是每个人都赞同阴谋论。[在 EEVBlog 论坛](https://www.eevblog.com/forum/projects/fu-dyson-bms-an-(unofficial)-firmware-upgrade-for-dyson-v6v7-vacuum-bms/)上，一些用户指出，执行不好的电池平衡程序可能比根本没有电池平衡程序更有问题。可能戴森在早期的包中对该技术有一些不好的体验，并决定远离它，并试图通过使用更高质量的电池来补偿。也就是说，至少有一个人能够通过安装这个非官方的固件来恢复他们自己“死亡”的电池组，所以不管是不是故意的，似乎没有什么争议，可用的电池确实被过早地标记为有缺陷的。

即使在 DIY 项目中，适当的电池平衡也是关键，所以我们不得不承认，戴森故意关闭他们包中的这个[重要功能](https://hackaday.com/2020/06/11/a-beginners-guide-to-lithium-rechargeable-batteries/)似乎有点不寻常。但是陪审团仍然不知道詹姆斯爵士是否试图欺骗他的顾客——正如汉隆的剃刀所说，“永远不要把可以用愚蠢来充分解释的事情归因于恶意”。

 [https://www.youtube.com/embed/dwyA5rBjncg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dwyA5rBjncg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

