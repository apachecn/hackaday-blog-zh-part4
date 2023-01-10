# 发挥全 g 代码控制的威力

> 原文：<https://hackaday.com/2022/10/30/playing-with-the-power-of-full-g-code-control/>

切片软件需要在易用性和控制之间保持平衡，同时处理你扔给它的任何 STL 文件。如果您消除了转换现有 3D 模型的需要，并直接创建 g 代码，您将获得很大的设计自由度，但代价是增加了设计工作量。通过利用这种自由并使其更易访问，[Andrew Gleadall]和[Dirk Leas]创建了 [FullControl 设计库](https://fullcontrol.xyz/#/models)。

每个模型都是一个数学生成的挤压路径，具有一系列可调整的设计参数和打印设置。这样你就可以打印出类似于[单层非平面部件](https://fullcontrol.xyz/#/models/971ff7)，或者[90°无任何支撑的突出物](https://fullcontrol.xyz/#/models/b70938)(休息后的视频)。该网站是使用 python 版本的[原始的基于 Excel 的 FullControl 设计器](https://hackaday.com/2022/07/01/full-printing-path-control-without-writing-gcode/)(在撰写本文时尚未发布)，以及用于 3D 可视化的 [threej](https://threejs.org/) s 构建的。

去浏览这个库，使用一些参数，看看有什么符合你的想法。关于想法、帮助和更新，请关注[完全控制子编辑](https://www.reddit.com/r/FullControl/)。

[https://www.youtube.com/embed/c9b7Ey4LyCs?feature=oembed](https://www.youtube.com/embed/c9b7Ey4LyCs?feature=oembed)

我们已经介绍了另一个基于网络的工具， [Gcode Designer](https://hackaday.com/2021/07/19/3d-print-in-the-air-with-a-little-software-support/) ，它的灵感实际上来自于 Full Control。

谢谢你的提示[基思·奥尔森]