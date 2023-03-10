# 应用科学推出电致发光控制器

> 原文：<https://hackaday.com/2018/11/26/applied-science-rolls-an-electroluminescent-controller/>

继发光二极管、薄膜晶体管、有机发光二极管和液晶之后，还有一种显示技术没有得到太多关注。电致发光显示器已经出现很久了，但仍然没有很多应用。这种情况可能很快就会改变，因为应用科学公司(Applied Science)找到了一种在任何东西上构建 EL 显示器的简单方法，并创造了一种简单的电路，能够在一种非凡的蓝色磷光 EL 显示器上驱动视频。

对于这个构建，[Ben]使用的是 Lumilor 的一种特殊产品[，它由一个类似铜的导电底层、一个透明的电介质、“lumicolor”磷光体和一个透明的导电顶层组成。所有这些层都是用喷枪涂抹的，图案是用桌面乙烯切割器制作的。这是一个完整的系统，设计用来在摩托车油箱上安装电致发光显示器，并让门像****一样发光。也就是说，该系统并不太依赖于基底，而且[Ben]已经成功地在塑料片、3D 打印部件甚至纸张上制作了 EL 显示器。](https://www.lumilor.com/)

与以前(和正在进行的)创造 EL 显示器的努力相比，如[【Fran】的阿波罗 DSKY](https://hackaday.com/2017/05/29/re-creating-the-apollo-dskys-display/) 的再现，Lumilor 系统似乎格外简单和干净。目前的努力就像[Fran]的例子一样，正在使用丝网印刷工艺，无论怎么看都是一团糟，不能应用于非平面。

[![](img/4efa052823d3d237ce19fe798e4ce686.png)](https://hackaday.com/wp-content/uploads/2018/11/4878161541658312551.png) 但是电致发光显示器不仅仅是在基板上放几层化学物质——你需要用高频、高压交流电来驱动这些显示器。为此，[【Ben】基于 Adafruit 小饰品 M0 设计了一个多通道电致发光驱动器](https://hackaday.io/project/162240-multi-channel-electroluminescent-driver)，两个 LT3468 ICs 产生高压，一个 HV507 或 HV513 驱动 8 或 64 个通道。

有了创建 EL 显示器和驱动 64 个通道的能力，实际上只需要做一件事:32×32 显示器。即使在 32×32 EL 显示屏上看到几行扫描也很神奇，但它还有另一个锦囊妙计:它还播放低分辨率视频*永远不会放弃你*。

这是一个不容错过的视频，请看下面。

 [https://www.youtube.com/embed/eUUupR-ongs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eUUupR-ongs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

