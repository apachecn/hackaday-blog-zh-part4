# 智能填充的有限元分析结果

> 原文：<https://hackaday.com/2019/02/06/finite-element-analysis-results-in-smart-infill/>

如果你想让 3D 打印更强大，只需添加更多材料。增加填充的密度，或添加更多周长。但你会遇到的问题是，你不需要在所有地方都添加更多的塑料，只需在承受最大压力的薄弱部位添加即可。研究零件最薄弱的地方是有限元分析的领域，是的，你可以在 Fusion 360 中完成。使用正确的技术，[你可以在你的 3D 打印机](https://www.youtube.com/watch?v=q0YsC53mFvY)上制造出更坚固的零件，【Stefan】在这里向你展示如何做到这一点。

这个建筑的灵感来自于(阿德里安·鲍耶)的博客，他在博客中谈到了向 3D 打印物体的内部添加“纤维”以增加强度。这些“纤维”根本不是真正的纤维，而是细长的圆柱形空隙。其理论是，切片器会将其解释为一个洞，并在这些空隙周围放置周界，从而有效地增加印刷品中局部区域的填充密度。将这与有限元分析结合起来，你会得到一个在需要的地方更坚固的部件，而且不会浪费塑料。

然而，有一种更简单的方法。Fusion 360 和 ANSYS 有限元模拟都是免费的工具，允许对导入的 3D 对象进行一定量的有限元分析。这可以用来找到任何 3D 打印最薄弱的部分，并且可以导出为 3D 网格。Slic3r 有一个修改器网格功能，将这种有限元分析网格(以 100%填充打印)与原始部件(以 10%左右填充打印)相结合，可以在需要的地方产生强大的东西，不会浪费塑料，并且比[阿德里安·鲍耶]的“纤维”技术更容易设置。

在打印了一些具有不同程度和填充技术的 3D 打印钩子后，[Stefan]发现在大约 50 千克负载的测试钩子中，2 个周长的基线失败了。智能填充钩在大约 100 千克时失效。不坏，花式裤钩仅重约 30%。

你可以在下面查看整个工具链和测试的视频。谢谢[Keith]送来这个。

 [https://www.youtube.com/embed/q0YsC53mFvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q0YsC53mFvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

