# 想念你的老诺基亚的预测文本吗？构建您自己的 T9 键盘

> 原文：<https://hackaday.com/2021/06/03/miss-the-predictive-text-from-your-old-nokia-build-your-own-t9-keypad/>

你想念你的旧诺基亚砖在打开预测文本时令人兴奋的打字速度吗？[Guy Dupont]也这么做了，所以他创造了一个内置 T9 预测文本的[USB 键盘](https://hackaday.io/project/179977-standalone-t9-predictive-keyboard)，将打字变成单手操作。休息后的视频。

T9 是第一个在 90 年代末和 21 世纪初获得广泛使用的预测文本技术。目标是通过将按键序列与可能单词的字典进行匹配，最大限度地减少在多按键键盘上打字所需的按键次数。它根据使用频率对单词进行优先排序，并能适应用户的偏好。【Guy】在 Circuit Python 中实现了 T9，主要针对树莓 Pi Pico 上使用的 RP2040 微控制器，插入任何设备都会以普通 USB 键盘的形式出现。字典存储在闪存中，可以使用[Guy]开发的工具进行更新。它还可以改变模式，为旧的多按打字，数字键盘，或宏垫。

我们很想知道用 T9 单手打字有多快，以及我们的读者能想象出什么样的应用。看起来这个实现并不能了解用户的偏好，我们认为这是一个值得添加的特性。

我们最近介绍了几种独特的定制键盘，有些比其他的更实用。在愚蠢的一面，这些包括一个[手榴弹形状的功能垫](https://hackaday.com/2021/04/18/this-pineapple-keyboard-is-the-bomb/)，一个[五按钮和弦键盘](https://hackaday.com/2021/05/06/the-keyboard-you-really-dont-need-or-want/)，和一个[微型双键键盘](https://hackaday.com/2021/01/23/two-key-keyboard-build-log-starts-small-but-thinks-big/)。

 [https://www.youtube.com/embed/6cbBSEbwLUI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6cbBSEbwLUI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)