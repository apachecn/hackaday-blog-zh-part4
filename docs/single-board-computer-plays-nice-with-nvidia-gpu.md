# 单板电脑玩 NVIDIA GPU 好看

> 原文：<https://hackaday.com/2018/11/10/single-board-computer-plays-nice-with-nvidia-gpu/>

说到单板电脑，就是方便。原始计算能力与尺寸之间的权衡意味着它们中的大部分最终都是基于 ARM 的，但也有一些例外，如基于 x86 的 Udoo Ultra。Udoo Ultra 上的嵌入式英特尔 405 GPU 比同类产品中的大多数都要好，但这不会开始在浏览器窗口之外播放任何东西。不满足于“标准”[Matteo]将他的构建[与 Udoo x86 Ultra 和 NVIDIA 1060 GPU](https://udoo.hackster.io/matteodelbalio/udoo-x86-with-geforce-gtx-1060-gpu-2aed20)结合在一起。拥有一个比它所连接的整个计算机长三倍的扩展卡似乎很荒谬，但从什么时候开始，荒谬阻止了人们对更多多边形的追求？

![M.2 adapter board trim comparison](img/43797ce2558756bb0f8ac5f9df1bf90b.png)

M.2 to PCIe adapter board (Top) Trimmed adapter board (Bottom)

因为 Udoo Ultra 没有 PCIe 插槽[Matteo]插在 M.2 到 PCIe 适配器板上。有两条 PCIe 线可以通过 Udoo Ultra 的 M.2 端口访问，尽管需要调整适配器板以适应。PCIe 母插槽被切开，让 1060 GPU 滑入。鉴于 Udoo Ultra 的限制，1060 GPU 的所有吞吐量都不会被利用。

Windows 10 是为这台机器选择的操作系统，这样所有的 NVIDIA 驱动程序都可以安装，还有一个额外的好处是可以偷偷加入一点 Trackmania Turbo。因此，为了配合构建，[Matteo]创建了一个图形比较视频，以展示嵌入式图形芯片的显著改进。你可以在下面的视频中看到 Time Spy 基准测试的结果。

 [https://www.youtube.com/embed/9Evkc3L-NJM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9Evkc3L-NJM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

