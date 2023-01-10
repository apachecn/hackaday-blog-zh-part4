# 小射线追踪器适合 64 字节

> 原文：<https://hackaday.com/2018/11/21/tiny-ray-tracer-fits-in-64-bytes/>

纵观人类历史，人们试图制造最大的，最快的，有时是最小的。[Hellmood]属于后一类，并用一个用于 MSDOS 的 64 字节[交互式 3D 光线投射应用](https://www.pouet.net/prod.php?which=78044)证明了这一点。

为什么是 MSDOS？我们想为什么不呢？的。COM 文件格式比较精简，不需要做很多工作就可以接管一切。如果程序很大，它不会给人留下深刻印象。目前有 64 种灰色阴影，看起来很奇怪，但是有使用各种调色板的版本，每一个都适合 64 字节或更少。甚至还有鼠标控制，你可以在下面的视频中看到结果。

甚至有一些不做 3D 和光线追踪的版本可以容纳 43 个字节，但这在视觉上并不令人印象深刻。正如您所料，代码是用汇编语言编写的:

我们查看了代码，发现有一个 BIOS 调用将视频模式设置为 13 hex，还有一些直接端口输出到 0x3C9 的 VGA 视频 DAC。在那之后我们迷路了，但是它确实是一个经济的程序，即使我们看不到它是如何阅读鼠标的。

如果你想自己做一些 MSDOS 编程，你可以[使用 gcc](https://hackaday.com/2018/05/14/msdos-development-with-gcc/) ,尽管你几乎肯定会得到更大的可执行文件。如果你只是怀念旧游戏和软件，你可以在[你的浏览器](https://hackaday.com/2016/02/05/a-dos-education-in-your-browser/)中运行它们。

 [https://www.youtube.com/embed/hEmK64CKpP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hEmK64CKpP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

