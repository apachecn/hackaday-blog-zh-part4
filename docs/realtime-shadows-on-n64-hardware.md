# N64 硬件上的实时阴影

> 原文：<https://hackaday.com/2021/12/26/realtime-shadows-on-n64-hardware/>

虽然任天堂 64 游戏机在许多人的心目中已经被归入“坚决过时的图形”时代，因为它的图形处理器(GPU)血统直接追溯到 SGI 在 20 世纪 90 年代提供的最好的，它也支持一系列现代功能，包括动态阴影。在一个简单的演示中，[lambertjamesd]演示了如何使用这个特性。

在演示视频中可以看到(休息后链接)，该演示采用了单个动态灯光，它在场景中的中心对象下方投射阴影，周围漂浮着一个猴子对象，它投射自己的阴影(渲染到[辅助帧缓冲区](http://gliden64.blogspot.com/2013/10/frame-buffer-emulation-intro.html))。这个辅助缓冲区然后被[混合](http://ultra64.ca/files/documentation/online-manuals/man/pro-man/pro15/index15.5.html)到主缓冲区，正如[在 Reddit 上 */r/programming* 上【ItzWarty】解释的](https://old.reddit.com/r/programming/comments/rmgk2n/realtime_shadows_on_nintendo_64_hardware_tech/hpo76p2/)。

这实际上意味着主场景使用了一个[阴影体](https://en.wikipedia.org/wiki/Shadow_volume)，它在*毁灭战士 3* 中被广泛使用。N64 没有在所有地方都使用阴影体积的主要原因是由于它对场景中的阴影投射者(对象)的限制，例如需要凸起，并且重叠可能会导致伪像和故障。

《毁灭战士 3》将通过使用模板缓冲来解决这个问题，这将进一步完善 N64 上的基本动态照明支持，最终将导致我们今天拥有的花哨的视频游戏图形。毫无疑问，在下一个十年里，它会像往常一样再次过时。

 [https://www.youtube.com/embed/_phjHpxyrbU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_phjHpxyrbU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

