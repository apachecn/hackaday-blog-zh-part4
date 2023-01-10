# 在 Apple II 上显示位图

> 原文：<https://hackaday.com/2018/10/05/displaying-bitmaps-on-the-apple-ii/>

Apple II 是广受欢迎的宠儿，真正开启了该公司的发展，后来为你带来了 iMac、iPod 和 iPhone 等宠儿。传奇人物史蒂夫·沃兹尼亚克的创意，这是一台低成本的家用电脑，利用一些有趣的妥协，用最少的组件创建视频输出。如果你想在 Apple II 上输出全位图图形，这会很困难——但这肯定是可能的。

【cybernesto】着手完成这个任务，[并在 GitHub](https://github.com/cybernesto/VBMP) 上发布了 VBMP。它以汇编语言编程，基于 democoder Arnaud Cocquière 的工作，在老式 6502 驱动的机器上显示位图图像。它可以显示 560 x 192 的单色图像或 140 x 192 的 16 色图像，加载速度很慢，但确实能完成任务。

我们在其他地方也看到了类似的发展——在这个老式的卫星跟踪器项目上。【Kepler matic】报告说他们的代码运行速度与 VBMP 加载器相似，尽管做了几件不同的事情。[你也可以在 GitHub](https://github.com/sup4rl33thax0r/keplermatik-map) 找到它，享受阅读的乐趣。

如果你想用你的老式硬件实现类似的东西，它值得一看。有了源代码，就可以轻松地将其集成到其他项目中。学习为这些旧机器编程可能很有挑战性，但这只是乐趣的一半——当你做出一些令人敬畏的东西时，[一定要把它放到提示栏](https://hackaday.com/submit-a-tip/)。