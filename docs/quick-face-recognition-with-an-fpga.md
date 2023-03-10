# 用 FPGA 实现快速人脸识别

> 原文：<https://hackaday.com/2018/11/25/quick-face-recognition-with-an-fpga/>

现在是 21 世纪，根据许多科幻电影，我们现在应该已经完善了人工智能，对吗？我们正在实现这个目标，这个项目来自一群康奈尔大学的学生，名为“ [FPGA kNN 识别](http://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2018/es876_aw528_bac239/es876_aw528_bac239/es876_aw528_bac239/index.html)”是面部识别的一次优雅的尝试。

对于外行来说，K-最近邻或 kNN 算法是一种非常简单的分类算法，它使用给定数据集和被检查的数据点之间的相似性来预测所述数据点属于哪里。在这个项目中，作者使用相机拍摄图像，然后保存其直方图，而不是整个图像。为了训练网络，相机拍摄各种面部照片，并创建一个直方图数据库，这些直方图被标记为同一张脸。这个过程对许多人脸重复进行，并且在附带的视频中显示为相对快速的过程。

分类或“猜猜是谁”的过程从相机中获取图像，并将其与所有已存储的人脸进行比较。系统会选择相似度最高的一个，结果非常棒，尽管这并不是最精彩的部分。使用 FPGA 实现，这意味着整个过程已经流水线化，以减少计算时间。这使得这个项目值得一看，特别是对于那些研究基于 FPGA 的开发的人来说。这是一个 k 距离计算器、排序器和选择器的硬件实现。请务必通读排序算法的文本，因为我们发现它非常有趣。

Arduino 最近发布了具有 FPGA 的 Arduino MKR4000 板，现在有许多开源板可供您轻松使用。我们希望在接下来的几年里能在会议徽章上看到这些。

 [https://www.youtube.com/embed/hYRiWG278oo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hYRiWG278oo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

