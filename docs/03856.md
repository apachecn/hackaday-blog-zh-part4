# 用这个手动真空抓放工具控制吸力

> 原文：<https://hackaday.com/2019/08/14/control-the-suck-with-this-manual-vacuum-pick-and-place-tool/>

表面贴装器件所用的胶带可能针对自动拾取和放置进行了优化，但那些试图手动挖掘元件的人会倒霉。无论包装的大小如何，胶带上的孔似乎都太小了，无法用镊子夹住它，所以你最终会把它夹起来，或者更糟，夹得太紧，把小东西扔进了空隙。我们希望你点了额外的。

这种情况就是真空处理器被发明的原因，尽管它们对于拾取和放置 SMD 很有用，但它们并不完美。[Steve Gardener]对这种工具的次优体验使他制造了[这种定制的真空取放工具](https://sdgelectronics.co.uk/youtube-videos/a-diy-smd-pick-and-place-tool-for-electronics-assembly/)。它是基于一个现成的韦勒单位，其中只有手机仍然存在。一个更大、更强大的真空泵通过一个带有 PIC18F13K22 微控制器的 PCB、一个电源、一个控制真空的螺线管和一个开关泵的继电器加入到一个定制的外壳中。脚踏开关启动泵并关闭真空排气口；松开踏板会打开通风口，让零件落下，同时泵会持续运行一段可变的时间。这使得他可以快速完成一系列的零件，而不必在两次拾取之间建立真空。下面的视频展示了运行中的构建和工具。

我们喜欢这个工具的想法，抛光的外观也非常光滑。不过，如果手动取放不适合你，也许可以试试[将 3D 打印机转换成自动 PnP](https://hackaday.com/2018/07/25/monoprice-mini-converted-to-pick-and-place-kinda/) 。

 [https://www.youtube.com/embed/1FnGqH_WkL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1FnGqH_WkL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

