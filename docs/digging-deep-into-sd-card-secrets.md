# 深入挖掘 SD 卡秘密

> 原文：<https://hackaday.com/2020/07/19/digging-deep-into-sd-card-secrets/>

对某些人来说，SD 卡就是 SD 卡，唯一值得注意的是它提供的存储容量，如标签上所印。然而，就像诗人一样，SD 卡包含*众多。*【杰森·金】对是什么让闪迪的 microSDXC 卡的高耐久性系列产生了兴趣，[所以他着手调查。](https://ripitapart.com/2020/07/16/reverse-engineering-and-analysis-of-sandisk-high-endurance-microsdxc-card/)

自然，客户服务是没有帮助的。相反，[Jason]开始刮掉隐藏卡的测试点的环氧树脂覆盖物。需要一些精细的焊接来将测试点连接到分线板，同时还需要将 SD 接口连接到计算机来完成它的工作。DS Logic Plus 信号分析仪用于分离进入芯片的信号，以了解芯片内部的情况。

在四处探查后，[Jason]能够取出 NAND 闪存 ID，当与东芝数据表进行比较时，表明该卡使用 BiCS3 3D TLC NAND 闪存。与传统的平面闪存技术相比，3D NAND 闪存有几个优势，如果 SanDisk 将这一点放在他们的宣传材料中，他们可能会节省[Jason]大量的调查时间。

我们以前见过其他类似的攻击，比如通过测试点执行的数据恢复。如果你一直在自己的工作室研究 SD 卡，[一定要让我们知道](http://hackaday.com/submit-a-tip)！