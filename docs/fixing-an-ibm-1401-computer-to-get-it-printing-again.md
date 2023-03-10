# 修理 IBM 1401 电脑，让它再次打印

> 原文：<https://hackaday.com/2018/09/20/fixing-an-ibm-1401-computer-to-get-it-printing-again/>

IBM 1401 是 IBM 在 20 世纪 60 年代推出的一款经典电脑，后来它使用了晶体管而不是真空管，这对这个故事来说可能是一件好事。对于小型企业，它通常与 1403 打印机一起用作主要的数据处理机器。对于拥有大型机的大型企业，1401 用于处理较慢的外围设备，如 1403 打印机和读卡器。

[![Broken germanium transistor](img/5f3b4c30da3f04ab042f76a98e3e463d.png)](https://hackaday.com/wp-content/uploads/2018/09/germanium-transistor-cr.jpg)

Broken germanium transistor

加利福尼亚州山景城的计算机历史博物馆有两台工作的 1401 以及至少一台 1403 打印机，最近每当打印机打印出一行时，计算机都会报告“打印检查”错误。[Ken Shirriff]是发现并解决问题的人之一，他写了一篇详细的博客文章,带我们从第一次缩小问题范围的测试开始，通过 IBM 的原始逻辑图，直到最终拉出可疑电路板并找到罪魁祸首，一个可能因腐蚀而失效的锗晶体管和一条看起来没有牢固连接的发射极线。他们怎么知道的？在典型的[肯]和公司的风格，我们喜欢，他们打开了晶体管，在显微镜下看着它。我们有一种感觉，如果他们能挖得更深，他们就会挖得更深。

如果你不熟悉这个维护博物馆机器的团队的工作，你会想了解一下[他们最近是如何让 1401 运行 FORTRAN II 代码](https://hackaday.com/2018/02/11/ibm-1401-runs-fortran-ii-once-more/)的。