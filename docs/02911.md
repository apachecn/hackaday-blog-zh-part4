# 由特别提款权收集的 GOES-17 全地球圆盘图像

> 原文：<https://hackaday.com/2019/05/03/full-earth-disc-images-from-goes-17-harvested-by-sdr/>

我们已经看到很多关于从我们头顶上呼啸而过的卫星上捕捉天气图像的黑客，但这篇来自[Eric Sorensen]的写得很好的操作指南采用了一种不同的方法。这篇文章不是从一天几次掠过头顶的极地卫星上捕捉图像，而是着眼于从 GOES-17 上捕捉图像，GOES-17 是一颗俯视太平洋的地球静止卫星。事实上，它是一颗地球静止卫星，这意味着它一直捕捉相同的视图，所以你可以捕捉到天气的精彩延时视频。

 [https://www.youtube.com/embed/qGS86jIHusE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qGS86jIHusE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



GOES-17 是一颗地球静止卫星，这意味着它涉及的内容更多一些。虽然在 800 公里左右高度运行的极地卫星可以用一根随机的电线接收，但地球静止卫星的 35，800 公里高度意味着你需要一个更好的天线。不过，这并不一定很贵:[Eric]使用了一个 100 美元的抛物面天线和一个[100 美元的 Airspy 迷你 SDR](https://airspy.com/airspy-mini/)接收器，连接到运行一些开源软件的 Ubuntu 笔记本电脑上，接收和解码卫星的 1.7GHz 信号。

另一个诀窍是弄清楚把盘子放在哪里。因为它是一颗地球静止卫星，这一部分必须仔细完成，因为抛物面天线只有一个小的接收角度。[Eric]为他的天线设计了一个适合三脚架的 3D 打印支架。

捕捉卫星气象图像是一件令人着迷的事情，这增加了另一个层次的兴趣，因为图像显示了地球的整个圆盘。随着时间的推移捕捉一系列，你可以看到风暴在海洋中旋转，并看到它们有多复杂。

如果你正在寻找一种更简单的方式来开始接收气象卫星图像，请查看这个[指南，转换旧电视天线和 USB 接收器来捕捉极地卫星图像](https://hackaday.com/2017/07/10/old-rabbit-ears-optimized-for-weather-satellite-downlink/)。