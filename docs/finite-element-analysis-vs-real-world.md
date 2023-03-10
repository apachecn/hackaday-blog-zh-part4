# 有限元分析与现实世界

> 原文：<https://hackaday.com/2021/05/27/finite-element-analysis-vs-real-world/>

在高级工程界，有限元法——或者更常见的，有限元分析——是一个真正的主食。随着功能更强大的家用电脑的出现，甚至你的家庭项目也能从中受益。这项技术本身是非常通用的，但是你通常会看到它被用于结构分析。然而，你可能想知道它与现实有多吻合。也就是说，如果分析显示你的零件的一部分是弱的(或强的),当你实际制造零件时，这种情况是否成立？[Fiveohno]想知道同样的事情，并决定[做一些测试](https://www.youtube.com/watch?v=kAlWcmqcJo8)，你可以在下面的视频中看到。

当然，与任何模拟一样，精确度将取决于您的数据输入和模型。但是如果你仔细工作，它应该与真实世界匹配得很好，所以看到真实世界的测试结果是很有趣的。事实上，Solidworks 的一个视频显示了类似的部分——不经意地——指出了不要做什么。例如，该分析中使用的力太低，并且零件处于相对较低的应力点，而不是处于最大应力点。

一般来说，有限元法处理的是微分方程的求解。这是一个复杂的话题，但简而言之，你把一个零件分解成许多小块(一个网格)，然后用简单的方程来表示这一小块。在实验的情况下，模型是用于自行车的悬挂摇杆连杆，该连杆受到很大的应力。

实际实验进行了将近 11 分钟。足够的压力会导致零件断裂。然后查看分析，您可以看到物理损坏与模拟结果非常接近。

相比虚拟模拟，我们更喜欢看到真实的生活。如果你想了解更多关于有限元分析的知识，而你没有参加我们的远程会议，你可以[观看重播](https://hackaday.com/2020/12/31/remoticon-video-the-mechanics-of-finite-element-analysis/)。如果你想把这项技术应用到你的[填充图案](https://hackaday.com/2019/02/06/finite-element-analysis-results-in-smart-infill/)，我们已经看到它完成了。

 [https://www.youtube.com/embed/kAlWcmqcJo8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kAlWcmqcJo8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

