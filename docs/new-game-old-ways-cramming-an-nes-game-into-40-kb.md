# 新游戏，老方法:把一个 NES 游戏塞进 40 KB

> 原文：<https://hackaday.com/2019/01/09/new-game-old-ways-cramming-an-nes-game-into-40-kb/>

为什么有人会费心为即将迎来 40 岁生日的游戏机系统创造新内容呢？也许只是为了挑战将一款游戏装入 40 千字节的存储空间。

至少这似乎是[Morphcat Games]即将发布的*微法师*背后的动机，这是任天堂娱乐系统控制台的一款新游戏，其灵感来自于*超级马里奥兄弟*。有趣的是，他们是如何在如此小的空间里塞进如此多的内容的。下面的视频详细介绍了这一点，这是一堂精彩的优化课。游戏逻辑本身是用汇编语言编写的，这当然比高级语言效率高得多。即便如此，这也占用了 32 kB 的 ROM，只剩下 8 kB 用于背景元素和前景精灵。

通过组合有限的精灵大小、将较小的精灵平铺成较大的角色，以及通过水平或垂直翻转来重复使用平铺，一个令人印象深刻的完整的动画角色调色板被开发出来。背景元素被类似地解构和重用，从而产生了一个用于为游戏生成所有地图的瓦片调色板，它只占用 60 个字节。将这些转化为可玩的关卡需要更多的镜像和一些水平移动，看起来像是一个非常吸引人的游戏场。

是的，这款游戏有 Kickstarter ,但我们主要好奇的是如何将一款可玩的游戏塞进这么小的空间。不要误解我们——我们也喜欢《T2 》,复古派的《T3 》,但是看到早期游戏开发者赖以运作的技巧真的会让创意源源不断。

 [https://www.youtube.com/embed/ZWQ0591PAxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZWQ0591PAxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



为我们挖出了这块宝石。谢谢！