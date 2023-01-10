# 这个准将 16 是 NTSC 制式的…不，等等，是 PAL 制式的！

> 原文：<https://hackaday.com/2019/06/01/this-commodore-16-is-an-ntsc-one-no-wait-its-a-pal-one/>

我们已经习惯了我们的计算机在外围设备和处理方面都足够强大，在软件的控制下几乎可以无限配置，但曾几何时情况并非如此。8 位一代家用电脑正朝着其能力极限努力，仅仅是为了在电视屏幕上显示一幅图像，而且每个组件都将被设置为只做它原本打算做的工作。因此，当不同的国家有不同的电视标准时，如主要是欧洲的 PAL 和主要是美国的 NTSC，每个市场就会有不同型号的相同机器。Commodore 16 就是这样一台机器，[Adrian Black]用定制 ROM、Arduino 和 Si5351 时钟发生器修改了他的 NTSC 型号,以便在两者之间切换。

PAL 和 NTSC C16 的区别有两个。视频芯片的时钟频率不同，ROM 内容也不同。[Adrian]的机器因此有一个更大的 ROM，包含两个版本，可通过其中一个高位地址线进行切换。晶体振荡器电路中的几个轨道允许他从 Si5351 模块中注入新的时钟，并且 Arduino 控制一切。通过一个非常简单的界面选择合适的 ROM 和时钟，重置按钮被捕获，当短按仍然重置计算机时，长按切换模式。

尽管有首席工程师[Bil Herd]作为 Hackaday 的同事，但令人遗憾的是，我们没有看到我们应该看到的那么多 Commodore 16s。最近的一个专题展示了一个 64k 的 C16 ，但是没有变成 C64。

 [https://www.youtube.com/embed/RwLsFSg0FdU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RwLsFSg0FdU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[伊恩萨默斯]的提示。