# 用于 3D 打印的通用非平面切片器值得考虑

> 原文：<https://hackaday.com/2022/04/23/a-universal-non-planar-slicer-for-3d-printing-is-worth-thinking-about/>

有人可能会认为，当谈到 3D 打印时，切片软件几乎是一个已经解决的问题。取一个 3D 模型，将其切成与层高度相等的平面层，并制作刀具路径，以便喷嘴可以一次创建一个层。然而，随着 3D 打印变得更加复杂和强大，这种“平面切片”方法最终将成为一种限制，因为一系列平面切片不一定是处理所有对象的最佳方式(也不是所有材料或工具)。)

[![](img/51291566340c8669d2db3b0ffa82b59a.png)](https://hackaday.com/wp-content/uploads/2022/04/cube-cone-50.png)

How a 20 mm cube looks when sliced in a cone-shaped plane.

[René K. Müller]致力于重新想象切片本身，并展示了使用非平面几何图形对 3D 模型进行切片的结果。有很多 20 毫米的立方体被切成各种不同几何形状的图片，所以一定要看一看。分页符下面嵌入了一段视频，涵盖了要点。

这都是前瞻性的东西，而且[René]肯定提出了一些令人信服的观点来支持对通用切片的需求；一种能够处理任何几何图形的系统，具有沿任何路径或方向进行处理的自由。这个概念也引发了其他有趣的问题。例如，当切割具有非平面几何形状的 20 mm 立方体时，产生的切片通常看起来很奇怪。为这样的切片创建刀具路径的最佳方法是什么？毕竟，一些切片几何形状显然对物体更好，但不能被正常的热端容纳(这就是一个[旋转，倾斜喷嘴](https://xyzdims.com/2021/02/26/3d-printing-conic-slicing-for-rotating-tilted-nozzle-rtn/)的作用。)

这种担心目前对大多数用户来说可能不是问题，但在这种情况下尝试走在前面是值得的。为了避免有人认为非平面切片没有实际用途，我们之前报道了[René]关于[非平面切片如何在没有支撑的情况下可靠地产生 90°突出端的演示](https://hackaday.com/2021/03/08/3d-printing-90-deg-overhangs-with-non-planar-slicing/)。

 [https://www.youtube.com/embed/0jjYimwpp70?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0jjYimwpp70?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

