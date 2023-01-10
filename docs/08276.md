# 学习理解周围环境的机器人

> 原文：<https://hackaday.com/2020/11/06/robots-learning-to-understand-their-surroundings/>

今天，很容易制造一个带有机载摄像头的机器人，并通过第一人称视角手动驾驶获得乐趣。但是梦想实现自主的建造者很快发现，在摄像头安装和自主执行“转到椅子”命令之间有很多工作要做。幸运的是，我们可以借鉴诸如潘博文、孙建凯等人的观点解析网络

当一幅相机图像进入计算机时，它仅仅是一大串代表红、绿、蓝颜色值的数字，而我们的机器人根本不知道那幅图像代表什么。在过去的几年里，计算机视觉研究人员已经为图像分类问题找到了很好的解决方案(“有椅子吗？”)和*分割*(“椅子对应哪些像素？”)虽然这对于构建在线图像搜索引擎很有用，但对于机器人导航来说还不够。

机器人需要将这些像素坐标转换成现实世界的布局，这就是 View Parsing Network 要解决的问题。在 [*用于感知周围环境的跨视图语义分割*](https://arxiv.org/abs/1906.03560)(DOI 10.1109/LRA . 2020 . 3004325)中有详细说明，该系统采用多个摄像机视图观察机器人的四周。图像分割的结果然后被合成为机器人周围环境的 2D 自顶向下分割地图。(“椅子在哪里？”)

作者记录了如何在虚拟环境中训练视图解析网络，并描述了将训练好的网络转移到物理机器人上运行的过程。今天，这个过程需要比“下载 Arduino sketch”更高的技能水平，但我们希望这种模块在未来变得更加即插即用，以实现更好、更智能的机器人。

[ [IROS 2020 展示视频(时长 10:51)](https://www.iros2020.org/ondemand/episode?id=2531&id2=DL%20for%20Visual%20Perception%20II&1604378975550) 需要免费注册，有效期至少至 2020 年 11 月 25 日。下面嵌入了一分钟总结。]

 [https://www.youtube.com/embed/5fCSEWh0qIA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5fCSEWh0qIA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

