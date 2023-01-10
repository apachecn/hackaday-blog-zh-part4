# 丝般光滑的树脂打印机时间流逝感谢机器视觉

> 原文：<https://hackaday.com/2021/09/18/silky-smooth-resin-printer-timelapses-thanks-to-machine-vision/>

观看 3D 打印机测试的魅力在你花了几个小时后会逐渐消失，在这种情况下，那些很酷的延时视频就派上用场了。问题是，除非曝光与扫描架的运动同步，否则它们看起来不稳定，不舒服。这在 FDM 打印机上很容易做到，但树脂打印机完全是另一回事。

或者他们是？[Alex]发现了一种制作树脂打印机华丽延时视频的方法，必须亲眼目睹才能相信。他的方法的优点是，它可以与任何相机一起工作，除了连接到打印机构建平台的一个小 LED 投掷器之外，不需要任何硬件。LED 充当一个基准点，OpenCV 可以在每一帧中轻松找到它，它可以指示照片拍摄时舞台的 Z 轴位置。然后，一个 Python 程序对这些帧进行分类，这样看起来就像是一次平稳的拉动就将树脂打印从大桶中拉出。

为了使事情更加顺利，[Alex]还使用帧插值来填充构建平台使用实时中间流估计(RIFE)在帧之间跳跃的间隙。光是这项技术的细节就值回票价，而且结果也很惊人。如果你想尝试一下，亚历克斯好心地提供了他的代码。仅仅为了尝试一下，几乎值得买一台树脂打印机。

你的未来有树脂打印机吗？如果是这样，你可能想看看 [[Donald Papp]的指南，看看 SLA 与 FDM 打印机相比的利弊](https://hackaday.com/2020/04/30/3d-printering-will-a-resin-printer-retire-your-filament-based-one/)。

 [https://www.youtube.com/embed/lBMnWHdesWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lBMnWHdesWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

