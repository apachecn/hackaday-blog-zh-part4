# Voja Antonic:设计立方体

> 原文：<https://hackaday.com/2019/02/07/voja-antonic-designing-the-cube/>

Voja Antonic 在 2018 年为 Hackaday Belgrade 设计了这个神奇的逆向计算徽章，它非常有趣，我们想把它带到美国，基本上不加改变。这意味着 Voja 有一些空闲时间投入到新的硬件赠品中:[魔方](https://hackaday.io/project/162237-the-cube)。因此，虽然他 11 月在 Supercon 的演讲表面上是关于徽章的，但他忍不住告诉我们他的新爱，以及隐藏在其中的一些极其聪明的功能。

[![](img/d863e670b444470dd8391e2492cae434.png)](https://hackaday.com/wp-content/uploads/2019/02/5518971541632166246_thumbnail.png) 有趣的是，我们设计的硬件有时能在创造者身上反映出如此多的东西。Voja 设计了当时南斯拉夫第一台广泛使用的家用电脑(并在杂志上发表了 DIY 计划！).数以千计的是从他们的工具包。Galaksija 是一个基于 Z80 的设计，带有一个定制的基本配置，只能勉强挤进可用的 4K ROM 中。因此，你不应该对复古徽章有一个工作键盘和一个漂亮的基本板上感到震惊。

但是让我们跳到立方体，因为那是一个更有激情的项目。从外表上看，它们是非常简单的设备，只有一个 USB 端口和一个可爱的漫射 LED 环。审美？极简主义？说实话，很漂亮。

Voja 经历了一些公认的 80 年代中期南斯拉夫最黑暗的时期，当时说出你的想法可能会让你进监狱甚至更糟。出于天性或需要，他有点颠覆性。魔方不会告诉你它是什么，但它是一个加密和解密工具，可以在将他们的魔方链接在一起并交换密钥材料的人之间实现一次性密码本式的不可破解的加密。

密钥材料也是在立方体本身中生成的。里面有一个晶体管击穿白噪声电路，产生一个基于量子力学的真随机数的恒定流。是的，他在项目中添加了一个 5 V 至 17 V 的升压转换器，只是为了获得良好的随机数。沃佳不胡来；他曾经为一家赌场游戏设备制造商工作，在那里随机性真的很重要。

[![](img/8c58a577ed3fab8a4ff4621c9887d099.png)](https://hackaday.com/wp-content/uploads/2019/02/dscn0469_thumbnail.png) 两个立方体之间的交流也几乎是完全保密的。事实上，这可能是立方体完成的最酷的把戏。里面有一圈铜箔，两个立方体通过电容*相互耦合*，而不是使用无线电或光或任何其他可窃听的传输方法。你必须站在一对带着电磁探头的通信立方体旁边，才能监听。

剩下的就很简单了，开放固件。(还有一个加速度计，为了好玩或者额外的随机密钥素材。)你可以验证自己，它确实做到了它所说的。这意味着，如果你对秘密通信很认真，对手唯一能接触到你的地方就是你把魔方拴在上面的电脑。这是 Voja 的最后一招。Supercon badge 本身是一台独立的小型计算机，具有易于审计的固件和极其简单的硬件。将它连接到多维数据集将在同步其多维数据集的两个人之间提供一个完整的、完全无法破解的加密通道。适合最偏执的人，无论你是否有理由这样做。

立方体作为实用加密通信信道的缺点？它没有太多的密钥材料，所以你的消息最好简短，如果你[重复使用密钥材料](https://hackaday.com/2017/05/10/how-a-hacker-remembers-a-pin/)，XOR 算法是有毒的。如果对手拿到你的魔方并向它索要随机数据，它就完全被破坏了。

这是 Hackaday 母公司在 Supplyframe 徽标的橙色注塑 3D 版本中的赠品之一。对于我们这些足够幸运不需要间谍级加密的人来说，这是一个有趣的秘密解码环和一个出色的设计。但与此同时，如果你绝对需要在最糟糕的情况下获得一条简短的消息，你会希望你已经在超级电脑上配对了。

 [https://www.youtube.com/embed/4WxPGLsdbB8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4WxPGLsdbB8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
