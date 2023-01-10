# 将游戏世界与“不可能的”神奇宝贝交易联系起来

> 原文：<https://hackaday.com/2021/12/07/bridging-game-worlds-with-the-impossible-pokemon-trade/>

任天堂从未正式支持将辛苦赚来的神奇宝贝从第二代 GameBoy 游戏世界转移到“高级时代”卡带中(反之亦然)，然而[go pier]通过[定制 PCB 和适量的逆向工程](https://www.youtube.com/watch?v=inMbtwmVlKQ)使这些非法交易对初露头角的神奇宝贝训练者来说稍微容易一些。

原始 GameBoy 上的第二代(神奇宝贝金、银和水晶)和 GameBoy Advance 上的第三代(神奇宝贝红宝石、蓝宝石、火红色、叶绿和祖母绿)之间的数据结构变化意味着这些墨盒之间的交易永远不可能——至少不能通过任何合法手段进行。相比之下，神奇宝贝交易在第一代和第二代游戏之间是可能的，从第三代及以后也是可能的，这使得从第二代到第三代的飞跃成为一个明显的缺失环节。

现代玩家已经通过将卡带保存文件转储到 PC 上克服了这一限制，此时任何神奇宝贝都可以被添加到保存文件中或从保存文件中减去。因此，这种方法依赖于自我控制以及正确的硬件。[go pier]的解决方案可以说要优雅得多，只需要很少的额外硬件。带有新旧 GameBoy 游戏连接线端口的简单 PCB 是两代人之间的物理桥梁。ARM Cortex 微控制器位于这些连接之间，在新旧之间转换游戏数据。

微控制器需要在各代之间转换数据结构，看起来很合适。不仅神奇宝贝的数据需要转换，而且在两代人能很好地相互交流之前，还需要一些其他的技巧。GameBoy Advance 上的 Pokémon 带来了新的功能，例如代表交易室中玩家的移动(即，你可以看到另一个玩家在你的屏幕上移动)，这也是必须解决的问题。

对神奇宝贝社区内交易合法性的担忧是多人游戏体验的一个奇怪但可以理解的副产品。例如，现代玩家必须警惕“被黑”的神奇宝贝，这往往会在交易后给他们的游戏世界带来故障。除了这些问题之外，一些神奇宝贝玩家只是渴望真正的神奇宝贝，作为促进公平和愉快的游戏体验的一部分。

这种第二代和第三代游戏世界之间的字面意义上的桥梁使社区非常接近一种“合法”的方式，将他们的神奇宝贝从古老的盒子转移到现代游戏中。任天堂有一天会正式批准第二代到第三代的类似设备交易吗？更疯狂的事情发生过。

我们在 Hackaday 上喜欢我们的 GameBoy hacks，所以为什么不看看这个项目，[用 FRAM](https://hackaday.com/2021/11/08/pokemon-time-capsule/) 取代你的 GameBoy 游戏中的电池支持的 SRAM？

 [https://www.youtube.com/embed/inMbtwmVlKQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/inMbtwmVlKQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

