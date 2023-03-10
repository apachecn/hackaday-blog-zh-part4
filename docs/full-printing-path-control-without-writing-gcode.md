# 无需写入 GCode 的完整打印路径控制

> 原文：<https://hackaday.com/2022/07/01/full-printing-path-control-without-writing-gcode/>

用户友好的切片软件可以说是使 3D 打印对大多数用户来说变得触手可及的关键软件组件。没有它，从 CAD 设计到印刷部件将需要几个小时，而不是几秒钟。作为一种权衡，你放弃了对酒店确切路线的大量控制，但大多数时候这是值得的。然而，对于一些特殊的用例，完全控制刀具路径是必要的。进入 [FullControl GCode Designer](http://fullcontrolgcode.com/) ，这个工具给你所有的控制权，而不需要求助于直接编写 GCode。

FullControl 采用了一种类似于 OpenSCAD 的方法，您可以逐行定义路径几何。需要一个圆形数组？选择圆特征，定义其原点、半径、起始位置和拉伸高度，并定义副本的间距和轴(包括 Z 轴)。需要一个数学定义的灯罩？定义函数，FullControl 生成 GCode。[非平面打印](https://hackaday.com/2022/04/23/a-universal-non-planar-slicer-for-3d-printing-is-worth-thinking-about/)，打印头同时沿所有三个轴移动，而不是停留在恒定的 Z 高度也是可能的。在广告之后的视频中，[Thomas Sanladerer]展示了他如何使用 FullControl 将功能相同的零件的打印时间从两小时减少到 30 分钟。

FullControl 是使用 Visual Basic 脚本在 Microsoft Excel 上构建的，其代价是很长的 GCode 生成时间。它也没有以图形方式显示定义的刀具路径，所以生成的代码需要粘贴到像 Repetier Host 这样的查看器中，以查看它在做什么。幸运的是，Python 的下一个版本有望改善这些缺点。

在过去的几个月里，我们还展示了一些其他的 GCode hacks，它们可以沿着样条路径弯曲现有的 GCode，还有一个 T2 Blender 插件可以修改切片对象的表面纹理。

 [https://www.youtube.com/embed/ZgytQDoaD5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZgytQDoaD5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/KlxuZ5JnA0k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KlxuZ5JnA0k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

