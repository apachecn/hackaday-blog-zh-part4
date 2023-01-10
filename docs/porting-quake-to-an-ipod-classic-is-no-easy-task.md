# 将 Quake 移植到 IPod Classic 上并不容易

> 原文：<https://hackaday.com/2020/01/25/porting-quake-to-an-ipod-classic-is-no-easy-task/>

我们不认为我们会在 Hackaday 上再次看到另一个涉及老化 iPod Classic 的黑客，但[Franklin Wei]为大约 13 年前发布的第六代 iPod 提供了一个全新的 Quake 端口，让我们大吃一惊。《雷神之锤》会成为黑客们能拿到的所有设备中的 90 年代 FPS 吗？

该端口基于 RockBox，这是一种为 iPod 和其他便携式媒体播放器定制的固件。这不是该设备上的第一款游戏。毁灭之源港已经存在多年了。[Franklin]决定使用[简单的 DirectMedia Layer (SDL)](https://en.wikipedia.org/wiki/Simple_DirectMedia_Layer) 来简化他的工作。但这并不意味着这是一项容易的任务，因为[富兰克林]描述了一些非常有趣的错误，这些错误让他在大约两年的时间里没有完成他的工作。

第一个问题是，他使用的 GCC 编译器显然没有优化时间关键的混音例程。[Franklin]决定适可而止，深入 ARM assembly，手动重写代码的这些部分。他设法挤出了大约 60%的速度增长。更好的是，他遇到了一个 bug 的主要例子，这个 bug 是由贯穿他代码的一个非常具体的声音样本长度触发的。值得庆幸的是，随着所有的排序，端口现在被释放，我们都可以享受我们的手抽筋周围的小屏幕，以粉碎一些低聚合怪物。

如果你需要修理你的第六代 iPod，不必担心，因为它们看起来并不难自己维修。如果电池寿命和磁盘空间不如以前，也可以选择[为冬天](https://hackaday.com/2016/07/02/the-2000gb-ipod-you-wished-for-in-the-00s-is-an-isore/)扩充。休息之后，请查看地震港口的运行情况。

 [https://www.youtube.com/embed/r6V-4AZ7pkA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/r6V-4AZ7pkA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

