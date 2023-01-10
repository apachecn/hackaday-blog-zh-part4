# 程序条形码合成就像黑白一样简单

> 原文：<https://hackaday.com/2020/10/10/procedural-barcode-synth-is-as-simple-as-black-and-white/>

在 Hackaday，我们对奇特而美妙的乐器并不陌生。[詹姆斯·布鲁顿]长期以来一直着迷于将条形码扫描仪作为音乐的输入来源，现在[有了一个程序条形码驱动的合成器](https://www.youtube.com/watch?v=ywpl4en4MI0)来添加到他不断增加的手工乐器收藏中。我们之前已经介绍过[的条形码吉他](https://hackaday.com/2019/09/26/barcode-guitar-plays-more-than-beep-bop/)，它将一串数字从 PS/2 输出转换成音高。这意味着要打印大量的条形码，因为每个球场都需要一个单独的条形码。可以想象，这是一个相当笨重的大仪器。

[詹姆斯]没有查看阅读器的文本输出，而是把它打开，放到示波器上。一旦进入，他发现了一个很好的来源，输出一个方波，对应于条形码看到的黑白线。由于[James]正在使用的条形码没有[正确的开始和停止代码](https://en.wikipedia.org/wiki/Code_39)，条形码阅读器会持续扫描。通常，它会停止激光器通过 USB 或 PS/2 连接发送文本。一个简单的 5v 至 3.3v 电平转换器将方波馈入一个小型电路板，后者输出音频。

一段展示类似技术的视频激发了[James]的这个项目。那个视频的创作者有一面巨大的墙，墙上有不同的黑白线条图案。[詹姆斯的]下一个聪明之处是有一个小的 HDMI 显示器来动态生成条形码。Raspberry Pi 4 通过 GPIO 读取各种按钮，并在屏幕上显示结果条形码。一个快速的 3d 打印外壳很好地完成了构建，使事情变得小而紧凑。所有的代码和 CAD 文件都在 GitHub 上[。](https://github.com/XRobots/BarcodeSynth)

 [https://www.youtube.com/embed/ywpl4en4MI0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ywpl4en4MI0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[詹姆斯布鲁顿]的可怕的项目！