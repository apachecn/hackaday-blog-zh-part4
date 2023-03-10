# DIY 视频显微镜

> 原文：<https://hackaday.com/2019/10/16/diy-video-microscopy/>

一般来说，拥有一台显微镜是一种非常有趣的爱好，但对于黑客来说，它是一种特别有用的组装和检查工具，因为我们正在地下室和车库里用“沙粒”大小的组件构建硬件。在一次假日旅行中，一位好心的朋友送给了他一台教育用显微镜。这款车很旧了，但它毕竟是卡尔·蔡司，产于前民主德国的耶拿。由于光学显微镜对他来说用处有限，[【void nill】着手将其数字化](https://medium.com/@voidnill_28965/eduval-4-microscope-with-raspberry-pi-and-1000-0-gb-harddrive-mod-f1a4b778a016)。

他选择了树莓派路线。Pi 和硬盘直接连接到显微镜的框架上，VGA 显示器通过转换器连接。最后，使用一些泡沫将 Pi 相机临时装配到一个目镜上。这是一个快速而肮脏的方法，不是最好的解决方案，但对[voidnill]来说效果很好，因为他想保持原来的显微镜完好无损。

标准 Pi 相机有一个广角镜头。它被设计成捕捉大图像并将其汇聚到小传感器区域。把它转换成微距模式是可能的，但是需要一个黑客。镜头被取下并“翻转”,固定在远离传感器的地方——通常借助于伸缩管。这使得镜头可以对非常小的区域成像，并将其聚焦在(相对)大的传感器上。这种黑客技术被用于“OpenFlexure”显微镜项目，你可以在[我们今年早些时候写的文章](https://hackaday.com/2019/01/26/3d-printed-microscope-stage-offers-precise-movement/)或者这个[更新的链接](https://openflexure.org/projects/microscope/)中读到。如果你想要更高的放大倍数和图像质量，OpenFlexure 提供了一种将相机传感器直接与 [RMS](https://www.rms.org.uk/) 螺纹显微镜物镜匹配的设计。自今年早些时候以来，这个开源显微镜项目已经取得了很大的进展，世界各地的许多民间人士已经成功构建了自己的版本。它提供了许多定制选项，如基本或高分辨率光学系统和手动或电动舞台，这使它成为一个很好的尝试项目。

如果 OpenFlexure 项目被证明是一个令人生畏的构建，您可以尝试一些更简单的东西。前往公共实验室，在那里[partsandcrafts]向您展示如何"[用树莓 Pi](https://publiclab.org/notes/partsandcrafts/11-26-2017/building-a-raspberry-pi-microscope) 构建一个基本的显微镜"。它借鉴了其他开源项目，但使事情变得更简单，更容易构建。

在下面的视频中，[voidnill]简要介绍了他的快速破解技术(德语)。如果你已经有了一些显微镜黑客，或者已经自己制作了一个，请在评论区告诉我们。

 [https://www.youtube.com/embed/ehU6QjHHMfw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ehU6QjHHMfw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

