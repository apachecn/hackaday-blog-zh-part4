# 浏览器中的开源 CAM 软件

> 原文：<https://hackaday.com/2021/03/01/open-source-cam-software-in-the-browser/>

3D 打印机、台式数控铣床/路由器和激光切割机已经大大提高了普通黑客能够处理的项目水平。当然，如果你必须手动编写 g 代码，这些机器永远不会看到这种程度的采用，所以 CAM 软件发挥了很大作用。最近，我们发现了一个由[Stewert Allen]创建的名为[奇莉:Moto](https://grid.space/kiri/) 的开源的基于浏览器的 CAM 包，它可以为你所有的桌面 CNC 平台生成 g 代码。

奇莉说了一句:Moto 不在云中运行。一切都发生在客户端，在你的浏览器中。这种方法存在性能上的权衡，但是它确实具有跨平台和不需要任何安装的固有优势。你可以点击上面的链接，并在几秒钟内开始生成刀具轨迹，这是很好的尝试。在机器设置部分，您可以选择数控铣床、激光切割机、FDM 打印机或 SLA 打印机。CNC 的特性应该可以完美地满足 90%的台式 CNC 需求。界面很直观，即使你以前没有任何 CAM 经验。请在休息后观看视频，了解这些功能的完整分类，以及不同部分的时间戳。

激光切割所需的所有功能都存在，并且它支持刮刀。如果你想从激光切割的零件层中构建一个组件，奇莉:Moto 可以自动切片 3D 模型，并将 2D 零件嵌套在平台上。3D 打印切片机功能正常，但可能不会很快取代我们的常规切片机。它非常强调手动添加支持，并且像 Ender CR30 这样的带式打印机已经得到支持。

奇莉:Moto 正在积极改进，看起来 Stewart 对社区的意见非常积极。完整的源代码可以在 [GitHub](https://github.com/GridSpace/grid-apps) 上获得，如果你愿意，你可以在本地机器上运行一个实例。

我们喜欢我们在奇莉身上看到的:Moto，老实说，我们很惊讶我们没有早点发现这一点。在 Autodesk 取消了 Fusion 360 的免费版本后，一些 CAM 用户可能仍在寻找替代品。我们认为这是一个很好的选择，你可能也想考虑一下 [FreeCAD](https://hackaday.com/2021/02/13/open-source-its-the-little-things/) 中的路径工作台。

 [https://www.youtube.com/embed/08795Sj22QE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLRoVgyRoWZps-MD0NigZhWNkAL6NRjXwN](https://www.youtube.com/embed/08795Sj22QE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLRoVgyRoWZps-MD0NigZhWNkAL6NRjXwN)



谢谢你的提示[布鲁斯]！