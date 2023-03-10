# 将毅力漫游者的观点放入卫星观点背景中

> 原文：<https://hackaday.com/2021/03/30/putting-perseverance-rovers-view-into-satellite-view-context/>

查看我们熟悉的地方的航空和卫星地图总是很有趣，看到的视角不同于我们通常的地面视角。当我们对一个地方不熟悉时，我们就会失去它的背景。比如说火星。因此[马修·厄尔]试图通过投影到欧空局火星快车的轨道图像上，给毅力号火星车的着陆视频提供一些背景。由此产生的视频(嵌入在中断下方)是一个有趣的观看，旁边是技术文字记录 [*将“坚持”着陆镜头重新投影到卫星图像*](https://matthewearl.github.io/2021/03/06/mars2020-reproject/) 。

在[着陆过程](https://hackaday.com/2021/03/19/a-technical-but-not-too-technical-explanation-of-landing-perseverance-rover-on-mars/)中，火星车位置和方向的一些遥测数据被实时传输，其余的被记录下来并在以后下载。令人惊讶的是，该项目完全基于视频像素，没有使用任何信息。这使得结果更加令人印象深刻，并且该技术可以更广泛地应用于其他项目。基础部分是 SIFT ( [尺度不变特征变换](https://en.wikipedia.org/wiki/Scale-invariant_feature_transform))，它是 OpenCV 工具箱中的众多工具之一。SIFT 发现了毅力号的视频帧和火星快车轨道图像之间的相关性，并将其输入用 Python 编写的处理管道，以便在 Blender 中渲染结果。

虽然这个项目的许多元素对于机器人视觉的应用来说听起来很诱人，但在文章的“最后一笔”部分中涉及到了一些挑战。脱落的隔热罩干扰了自动跟踪，这意味着这个过程需要帮助才能正确理解动态变化的环境。此外，它的运行速度似乎不足以满足机器人的实时需求。但乍一看，这些问题都不是根本性的。他们只是等待一些有动力的人在未来去解决。

这个过程与投影映射有一些表面上的相似之处，投影映射是我们在[这些页面](https://hackaday.com/2019/10/31/be-anyone-or-anything-with-facial-projection-mask/)上介绍的一类项目[。除了一切都颠倒了(相机代替视频投影仪等。)让数学变成了一个完全不同的难题。但是如果你对投影贴图更感兴趣的话，](https://hackaday.com/2020/07/06/filmmaking-from-home-with-projection-mapping/)[这里是一个起点](https://hackaday.com/2018/09/16/raspberry-pi-projection-mapping-crash-course/)。

[via[Tanya Harrison 博士@TanyaOfMars](https://twitter.com/tanyaofmars/status/1371471473903276038)

 [https://www.youtube.com/embed/7kflC1nU0OM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7kflC1nU0OM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

