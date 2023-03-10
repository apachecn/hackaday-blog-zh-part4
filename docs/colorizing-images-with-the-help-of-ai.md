# 借助人工智能给图像着色

> 原文：<https://hackaday.com/2019/11/18/colorizing-images-with-the-help-of-ai/>

这个世界从来就不是黑白的——我们只是缺乏捕捉全彩色的技术。许多人已经试验了拍摄黑白图像和彩色图像的技术。[【Adrian rose Brock】决定让一个人工智能来做这项工作，结果令人印象深刻。](https://www.pyimagesearch.com/2019/02/25/black-and-white-image-colorization-with-opencv-and-deep-learning/)

该方法涉及在大量照片上训练卷积神经网络(CNN)，这些照片已经转换到实验室色彩空间。在这个色彩空间中，图像由 3 个通道组成——亮度、a(红绿)和 b(蓝黄)。使用这种颜色空间是因为它比 RGB 更符合人类视觉系统的特性。然后训练该模型，使得当给定亮度通道作为输入时，它可以预测可能的 a & b 通道。然后，这些可以重新组合成彩色图像，并转换回 RGB 供人们使用。

这是一种能够在多种材料上做好工作的技术。像草地、乡村和海洋这样的东西处理得特别好，然而更复杂的场景可能会有一些偏差。不管怎样，这是一种有用的技术，而且远没有手工方法那么繁琐。

CNN 也在做其他伟大的事情，从给西红柿命名到帮助家庭自动化的 T2。休息后的视频。

 [https://www.youtube.com/embed/r3Mmh_k2F0E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/r3Mmh_k2F0E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通用电气公司