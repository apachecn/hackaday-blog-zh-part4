# 从 3D 打印中识别 3D 打印机

> 原文：<https://hackaday.com/2019/02/17/identifying-a-3d-printer-from-a-3d-print/>

我最近看的一个电视犯罪节目集中在法医科学家识别塑料袋来自某一卷的能力上:很明显，这完全取决于条纹。然而，这一发展并不是虚构的:布法罗大学的研究人员已经发现如何[识别产生特定打印的单个 3D 打印机](http://www.buffalo.edu/ubnow/campus.host.html/content/shared/university/news/ub-reporter-articles/stories/2018/10/3d-printer-fingerprints.detail.html)。这项名为 PrinTracker 的开发利用打印机放置打印材料方式的独特差异来识别打印机，据称准确率达到 94%。

PrinTracker 背后的研究者是布法罗大学计算机科学与工程系的副教授许。他在 2018 年 10 月的一次会议上展示了[细节(PDF 链接)](https://cse.buffalo.edu/~wenyaoxu/papers/conference/xu-ccs2018.pdf)并描述了它的工作原理。在这项研究中，他们在 14 种不同的打印机上打印出钥匙，然后用高倍显微镜检查每一个指纹。特别是，他们扫描了指纹，以检查指纹的条带和附件纹理。条带是模型表面上由铺放的细丝产生的纹理，它是由打印头出口的进给速率、温度和形状产生的。附着纹理是层彼此附着的方式。当他们检查样本印刷品时，他们发现，经过一些图像分析和数字处理后，他们可以以相当高的统计准确性识别出是哪家印刷商生产的印刷品。

对于那些想了解这种分析如何工作的人来说，这是一本有趣的读物。[徐]推测，这可能对枪支和伪造案件的执法有用，该论文还研究了像刮擦或加热指纹这样的技术是否会模糊识别。

谢谢你的提示，[Sascho]！