# 使用雷达识别活动

> 原文：<https://hackaday.com/2020/09/06/recognizing-activities-using-radar/>

在保护老年人和弱势群体的隐私和独立性的同时照顾他们是一项具有挑战性的任务。在紧急情况下，按下紧急按钮或寻求帮助可能是不可能的，但持续的监督或摄像头监控往往既不实际也不周到。麻省理工学院 CSAIL 的研究人员几年来一直在研究这个问题，并提出了一个可能的解决方案，名为[射频日记](http://rf-diary.csail.mit.edu/)。使用射频信号、平面图和机器学习，它可以识别活动和紧急情况，穿过障碍和黑暗。如果这听起来很熟悉，那是因为它建立在 CSAIL 之前的[研究基础上。](https://hackaday.com/2018/07/02/using-an-ai-and-wifi-to-see-through-walls/)

使用的射频系统是有效的调频连续波(FMCW)雷达，它扫描 5.4-7.2 GHz 射频频谱。射频系统的分辨率有限，无法识别大多数物体，因此平面图提供了房间、床、桌子、水槽等具体特征的大小和位置信息。这些信息有助于机器学习模型识别周围环境中的活动。有效地训练活动字幕模型需要成千上万的训练示例，这目前对于 RF 雷达是不可用的。然而，有大量的视频数据集可用，因此研究人员采用了“多模态特征对齐训练策略”，这允许他们使用视频数据集来完善他们的射频活动字幕模型。

这种解决方案仍然存在一些隐私问题，但研究人员确实提出了一些改进措施。一个有趣的想法是，被监控的人通过顺序执行一组特定的活动来给出“激活”信号。

 [https://www.youtube.com/embed/j528nQs4_a8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j528nQs4_a8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



雷达是一个复杂但迷人的话题，我们已经在该领域看到了许多优秀的项目，包括可以用于生成航空图像的[自行车安装雷达](https://hackaday.com/2019/08/15/bike-mounted-synthetic-aperture-radar-makes-detailed-images/)和根据基本原理设计的[多普勒雷达模块](https://hackaday.com/2019/05/31/a-doppler-radar-module-from-first-principles/)。

感谢[Qes]和[ 亚当·康纳-西蒙斯 ]的提示！