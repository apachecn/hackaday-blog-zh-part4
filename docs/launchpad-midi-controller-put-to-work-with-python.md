# 使用 Python 启动 pad MIDI 控制器

> 原文：<https://hackaday.com/2018/11/04/launchpad-midi-controller-put-to-work-with-python/>

对于那些可能不会把空闲时间花在狂欢派对上的黑客读者来说，Novation 的 Launchpad 是一个受欢迎的外设，用于使用 Ableton Live 等工具创作数字音乐。它的 8×8 网格的 RGB LED 背光按钮用于通过 USB 向计算机发送 MIDI 命令来触发不同的节拍和剪辑。虽然不是演奏数字音乐的严格要求，但它也有助于让你在使用时看起来像是在驾驶宇宙飞船。

[![](img/e5347a94f6accab3a87889859e2abd99.png)](https://hackaday.com/wp-content/uploads/2018/11/lphk_detail.png) 这绝对是一个光滑的装置，但有限的库存功能意味着你不太可能在 Beat 实验室之外看到一个。尽管这可能很快会改变[多亏了由【艾拉·詹姆森】](https://github.com/nimaid/LPHK)创建的 LPHK。她用 Python 编写了一个程序，允许你将 Novation Launchpad 用作通用输入设备。但是，LPHK 没有简单地将硬件转换成 USB HID 设备或类似的东西，而是实现了一组令人印象深刻的功能，包括它自己的内部脚本语言。

在休息后的视频中，[Ella]向我们介绍了一些基本的使用案例，例如启动程序或用单独的按钮控制系统音量。LPKH 有一个 GUI，它提供了 Launchpad 的虚拟表示，并允许配置每个按钮的颜色和功能，以及保存和加载完整的布局。

对于更高级的功能，LPHK 使用了一种脚本语言，这种语言的灵感来自 Hak5 USB 橡皮鸭。脚本是用简单的英语命令和非常简单的语法编写的，这意味着您不需要有任何编程经验就可以创建自己的函数。还有一个脚本调度系统，板上有视觉反馈:如果一个按钮发出红光，这意味着有一个脚本等待执行。当按键快速闪烁时，脚本正在运行。第二次点击该按钮将会把它从队列中删除或者终止正在运行的脚本，这取决于你点击它时的状态。

[Ella]表明该软件仍在开发中；它不像她希望的那样完美，仍然有缺陷，但对于任何希望从 150 美元的 Launchpad 中获得更多功能的人来说，它绝对是有用的。她正在积极地寻找 beta 测试人员和反馈，所以如果你已经有了这样的一个板，试一试，让她知道你的想法。

过去我们已经看到黑客们[摆弄为他们的 Launchpad 控制器](https://hackaday.com/2015/09/30/novation-launchpad-midi-controller-moves-toward-open-source/)发布的开源 API 更新，但是总的来说还没有对这些设备做很多工作。也许随着像这样的强大软件的开发，这种情况很快就会改变。

 [https://www.youtube.com/embed/zZPt_lknhks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zZPt_lknhks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 KittenVillage 的提示。]