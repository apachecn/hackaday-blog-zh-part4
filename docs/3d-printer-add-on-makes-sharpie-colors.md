# 3D 打印机附件可产生清晰的色彩

> 原文：<https://hackaday.com/2021/07/29/3d-printer-add-on-makes-sharpie-colors/>

我们都见过 3D 打印夹具，它在灯丝进入热端时使用永久记号笔给灯丝上色。[Sakati84]有着完全不同的想法。打印头上的一个支架可以[拿起几支笔中的一支，用它给热端刚刚放下的那一层上色](https://github.com/Sakati84/3DPrintColorizer)。在下面的视频中，它看起来工作得很好，虽然我们想象它将是一只熊来校准高度，但它似乎可以用几乎任何传统的打印机来复制。

从逻辑上来说，你在没有笔的情况下打印一层，当你拿起笔时，它需要比打印喷嘴低一些，否则你会在新的塑料中拖动。

根据你想用的笔的品牌，你必须 3D 打印出一个架子和一些笔筒。还有适合热端的支架。您可以在视频中看到头部如何从机架上拿起和释放笔。这个架子最多能装六支钢笔。

切换笔需要大量的 Z 轴运动，因此我们预计打印速度总体上相对较慢。项目 wiki 中有关于提高 Z 速度和校准技巧的讨论，但它仍然不会那么快。

对于软件，有一个 Cura 后处理脚本。该软件认为有七台挤出机，第一台用于未上漆的长丝。挤压机 2-7 是虚拟的，并且在印刷每一层后将导致印刷获得颜色。

总的来说，这看起来像一个有趣的项目，即使我们担心我们的 Z 轴杆的健康。我们很想知道是否有人接受挑战，将其应用于其他打印机。

我们以前曾以更手动的方式玩过[虚拟挤压机](https://hackaday.com/2016/12/27/liars-3d-printing-multiple-colors-with-one-extruder/)。或者，就硬着头皮多加一些[真正的挤出机](https://hackaday.com/2021/03/07/this-dual-extrusion-system-rocks/)。

 [https://www.youtube.com/embed/2vPkmsyEDaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2vPkmsyEDaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

