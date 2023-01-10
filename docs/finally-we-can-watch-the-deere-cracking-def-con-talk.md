# 我们终于可以看迪尔破解 Def Con 的对话了

> 原文：<https://hackaday.com/2022/09/12/finally-we-can-watch-the-deere-cracking-def-con-talk/>

几周前，一些诱人的社交媒体帖子出现在 Def Con talk 上，其中[病态代码]闯入了现场直播的 John Deere 拖拉机的屏幕控制单元，并在其上播放了一个特殊的以 Deere 为主题的 *DOOM* 关卡。当时没什么可说的，但是[我们很高兴地发现整个谈话已经被放到了网上](https://www.youtube.com/watch?v=z2_TLz9TpwY)。

讲座首先介绍主题、机器内控制单元的基础知识以及各种不同年代的 Deere 屏幕单元。我们发现早期的机器仍然在世界各地的农场工作，它们依赖于过时的 Windows CE 版本，尽管最新的屏幕运行的是 Linux 版本。

这是他关注的最后几个屏幕之一，我们可以深入了解它的一些秘密。经过大量的死胡同和学习练习后，最终结果被提炼到硬件部分的弹簧针适配器中，这是一项足够简单的`cron`工作，通过保持文件系统可写来绕过 Deere 的一项防御措施，从而可以更新文件。关于特殊的*末日*等级也有更多的细节，作为一个特殊的奖励。

你可以看到[我们最初提到的这个演讲](https://hackaday.com/2022/08/17/did-you-see-a-john-deere-tractor-cracked-at-def-con/)，或者[阅读一些我们过去的迪尔报道](https://hackaday.com/2017/03/24/the-icon-of-american-farming-that-you-now-have-to-hack-to-own/)。

 [https://www.youtube.com/embed/z2_TLz9TpwY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z2_TLz9TpwY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[泰勒·芬利]的提示！