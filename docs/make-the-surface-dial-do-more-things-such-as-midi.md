# 让 Surface Dial 做更多的事情，比如 MIDI

> 原文：<https://hackaday.com/2018/09/04/make-the-surface-dial-do-more-things-such-as-midi/>

表面拨号是一个 100 多美元的旋转控制。你可以转动它，它会让一些基本的东西在你的微软 Surface 上发生。它是银色的，光滑而优雅，但从根本上来说，它只是通过模拟键盘快捷键来工作。这对于以一种良好的方式将模拟旋转运动转化为数字反馈并没有太大的帮助，[因此[SaveTheHuman5]创建了 Elephant 来解决这个问题。](https://hi.computer/elephant/)

作为标准，作为最终用户，有两种方式使用 Surface Dial。最简单的方法是使用现有的实用程序将拨号操作映射到快捷键。然而，对于用户界面中的旋钮和滑块来说，这是笨拙的。相反，[SaveTheHuman5]深入研究并使用微软提供的 Surface Dial API 创建了自己的实用程序。这使得原始数据可以从表盘中捕捉，并处理成你内心渴望的任何交互——只要你有编码肌肉来做！

大象软件允许旋钮在两种不同的模式下使用——鼠标捕捉和 MIDI。鼠标捕获允许用户使用常规鼠标选择 UI 对象，如音乐应用程序中的旋钮，然后转动表面转盘来调整控制。任何曾经在 VST 合成器上与微小的模拟旋转控制进行过斗争的人都会立即知道这一点的价值。然而，在 MIDI 模式下，旋钮本身只是一个直接输出命令的 MIDI 设备，这在演奏环境中尤其有用。

总的来说，这是一个相当有限的硬件的整洁的黑客——我们唯一想看到的是关于它是如何完成的更多细节。如果你对此有好的想法，请在评论中写下来。而且，如果你对旋转控制器的渴望仍然没有满足，[看看这个媒体控制器。](https://hackaday.com/2015/01/17/dial-is-a-simple-and-effective-wireless-media-controller/)休息后的视频。

 [https://www.youtube.com/embed/mxmSY4UDdQU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mxmSY4UDdQU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

