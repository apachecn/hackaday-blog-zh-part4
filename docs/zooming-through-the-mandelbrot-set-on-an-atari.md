# 在 Atari 上放大 Mandelbrot 集

> 原文：<https://hackaday.com/2021/07/09/zooming-through-the-mandelbrot-set-on-an-atari/>

根据维基百科，Mandelbrot 集合是“函数![f_{c}(z)=z^{2}+c ](img/98dfcc630973e738d9aed6369337c490.png)不发散的复数![c ](img/34285f016c0e6c5b228b7ba506cfd879.png)的集合。”即使你不理解它背后的数学原理，你也可能见过通过放大 Mandelbrot 集合的边界生成的复杂的分形图像。[Scott Williamson]不仅在雅达利[上获得了这个场景，还成功地制作了结果的动画视频。](http://blog.workshop88.com/2021/04/04/atari-8-bit-mandelbrot-set-zoom-videos/)

![](img/31a4717dda4ee14c68d5c57d8b124968.png)

Emulators were key to the project’s success.

做这项工作绝非易事。虽然只需要 10 行 Atari BASIC 就可以在 Atari 800 上渲染场景，但制作动画并将其转换为现代视频格式却需要很大的努力。[Scott]使用 Atari800Win-PLus 模拟器放大分形曲线上的多个位置，并记录了一个周末的结果。

然而，将各种帧合成为平滑滚动的视频需要更多的努力，需要一个 Python 脚本和`ffmpeg`来将所有东西缝合在一起[成你在 YouTube 上看到的结果。](https://www.youtube.com/watch?v=f-0igWKCl3s)最终的视频与来自亚当·斯波卡的[雅达利 chiptune 音乐结合在一起，帮助演示更加完美。](https://adamsporka.bandcamp.com)

结果让人想起一个老派的演示，即使这里的一切都是在现代计算机上从原始的 Atari 输出慢慢组装的。我们以前也见过其他伟大的 Mandelbrot 壮举，[像这个基于 FPGA 的实时浏览器](https://hackaday.com/2012/10/23/exploring-the-mandelbrot-set-in-real-time/)。休息后的视频。

 [https://www.youtube.com/embed/f-0igWKCl3s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f-0igWKCl3s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

