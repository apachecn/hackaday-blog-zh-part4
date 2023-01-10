# Arduboy，移植到桌面，然后再移植回来

> 原文：<https://hackaday.com/2019/07/18/the-arduboy-ported-to-desktop-and-back-again/>

最近一个整洁的小黑客项目是 Arduboy。这个微型游戏机看起来像是 O.G. Game Boy 的缩小版，但它显然是为黑客设计的。总之，它基本上是一个带有显示屏和几个按钮的 Arduino 板。

[rv6502]得到了一个 Arduboy，并意识到虽然有一些 3D 游戏，但没有填充多边形的东西，或真正类似于现代 3D 引擎的东西。[这必须被纠正](https://rv6502.ca/post/2019/01/05/starduino-3d-gaming-in-28kb-behind-the-pixels/)，结果非常接近微控制器上的 Star Fox。

这个项目首先在 Arduboy 上进行一个简单的测试，看看是否有可能以任何合理的速度渲染 3D 对象。[这个测试只是一个旋转的立方体](https://www.youtube.com/watch?v=rdJgbRAnAug)，一切看起来都很好。然后开始了一个漫长的过程，计算引擎可以跑多快，哪种显示器最适合有机发光二极管，以及如何在控制有限的 3D 世界中进行交互。

考虑到这是一个相当重要的工程项目，产生代码的最快方法不是在微控制器上调试代码。这个项目需要一个本地 PC 端口，因此所有的测试都可以在 PC 上进行，而不必每次都对 Flash 进行编程。那让[rv]扔掉了 Arduino IDE 和 USB 库；如果你在 PC 上写所有东西，最后只上传一个十六进制文件到微控制器，你根本不需要它。

Arduboy 图形功能的一个重大进步来自对有机发光二极管寻址模式的探索。默认情况下，显示器处于“水平模式”,适用于 2D 位图传送，但不适用于多边形栅格化。另一方面,“垂直寻址模式”允许一块 8 x 128 字节的内存直接映射到显示器。把这些字节推过来，就不需要数学来显示图像了。

简单地说，这是我们见过的最好的软件开发版本之一。它充满了巧妙的技巧(比如，如果你永远不需要结果，就不要做数学计算)，并将动画填充到比你预期的少得多的字节中。你可以看看下面的演示视频。

 [https://www.youtube.com/embed/ES3fGLuse4s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ES3fGLuse4s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

