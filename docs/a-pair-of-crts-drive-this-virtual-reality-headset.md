# 一对阴极射线管驱动这个虚拟现实耳机

> 原文：<https://hackaday.com/2020/01/23/a-pair-of-crts-drive-this-virtual-reality-headset/>

得益于几十年来小型化技术的进步，回顾过去的设备可能会很有趣。拿摄录机；我们真的扛着这些巨大的设备到处走，只是为了记录去迪士尼世界的家庭旅行吗？我们做到了，但是即使那些日子已经过去很久了，硬件仍然存在于壁橱和旧货店中。

这些摄像机可以变成很酷的东西，比如这个基于 CRT 的虚拟现实耳机。[安迪·韦斯特]从 T2“reggie vision”时代后不久的一对废弃的松下摄录机上拆下取景器，尽可能完整地保留外壳和光学元件。他对连接进行了逆向工程，并将复合视频输入连接到 HDMI-composite 转换器，该转换器连接到 Raspberry Pi 4 上的双 HDMI 端口。LM303DLHC 加速度计提供头部跟踪，所有东西都安装在一个为使用手机进行虚拟现实而设计的耳机上。就所用的粗电缆和大型组件的数量而言，最终的构建令人惊讶地整洁，它与攻击直升机飞行员使用的瞄准头盔有些许相似之处。

该软件融合了所有可行的东西——基于浏览器的 3D 动画的 Three.js、加速度计的一些现成驱动程序，以及将它们粘合在一起的 Python 和 shell 脚本。下面的视频展示了构建和演示；我们看不到[安迪]在辉煌的单色标清中看到的东西，但他似乎被深深打动了。我们也是。

我们已经看到最近使用 CRT 取景器的项目有所增加，包括[这个微小的矢量显示器](https://hackaday.com/2020/01/14/camcorder-viewfinder-converted-to-diminutive-vector-display/)。在所有的旧摄像机被抢购一空之前，是时候去逛逛旧货店了。

 [https://www.youtube.com/embed/p12QaZUZDnM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p12QaZUZDnM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

