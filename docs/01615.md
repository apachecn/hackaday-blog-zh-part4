# 项目展示了如何使用机器学习来检测行人

> 原文：<https://hackaday.com/2019/01/14/project-shows-how-to-use-machine-learning-to-detect-pedestrians/>

大多数人都熟悉机器学习可以用来检测物体或人之类的东西的想法，但对于任何不清楚这一过程实际上如何工作的人来说，应该看看[Kurokesu]的用于检测行人的示例项目。它详细介绍了使用什么软件，如何配置，以及如何使用数据集进行训练。

该应用程序使用 USB 摄像头，后端工作由神经网络的开源框架 [Darknet](https://pjreddie.com/darknet/) 完成。在那个框架上运行的是 [YOLO](https://pjreddie.com/darknet/yolo/) (你只看一次)实时物体检测系统。为了获得有用的结果，系统必须对大量样本数据进行训练。[Kurokesu]解释说，虽然可以使用预先训练的网络，但仍有必要通过添加更接近预期应用的数据集来微调系统。培训本身就是一种平衡行为。在模型数据集上过度训练的系统(或在太小的数据集上训练的系统)将遭受过度拟合，这是一种系统最终过于挑剔而无法有效概括的情况。在行人检测方面，这导致了假阴性——行人没有被标记出来，因为系统对行人应该是什么样子的想法过于严格。

[Kurokesu]关于行人检测的演练很棒，但是对于那些有兴趣后退一步并推出自己的项目的人来说，[这个 Darknet](https://github.com/AlexeyAB/darknet) 的分支包含 Linux 和 Windows 的 YOLO，并从更一般的角度包括关于安装、使用和培训的实用笔记和指南。有兴趣了解更多机器学习基础知识吗？别忘了[谷歌有免费的在线速成课程](https://hackaday.com/2018/05/22/machine-learning-crash-course-from-google/)让你快速上手。