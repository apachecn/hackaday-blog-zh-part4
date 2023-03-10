# 重新想象十字龙门 3D 打印机

> 原文：<https://hackaday.com/2020/08/19/re-imagining-the-crossed-gantry-3d-printer/>

简单地拥有一些 3D 打印机运动系统设计并不是停止探索它们的理由，因为即使是对现有架构的小迭代也可以产生一些巨大的改进。在过去的几个月里，【 [Annex_Engineering](https://github.com/Annex-Engineering/Chhogori-K2-Summit-Edition) 】和【 [wesc23](https://github.com/wesc23/CroXY) 】都在试验一种源自轨道的交叉龙门架构，这种架构后来被称为“CroXY”。从 Ultimaker 的使用杆的十字门架、Hypercube Overkill 项目甚至彼此借鉴概念，结果是两个紧凑的机器框架能够以极高的速度进行美丽的打印——在[Annex _ Engineering]的情况下超过 400 毫米/秒！

两种龙门设计都采用旋转的 MGN12 轨道(类似于[轨道芯](https://railcore.org/))并穿过其中两个轨道，像 Ultimaker 一样在交叉点安装托架。每个交叉的轨道控制一个具有普通笛卡尔运动学的自由度，但每个自由度也有一个冗余电机来增加扭矩。像 [CoreXY](http://corexy.com/) 设计一样，这种设置是为高速清晰打印量身定制的，因为与运动相关的电机已从移动质量中移除。然而，整个带的长度已经大大减少，导致更严厉的设置。

但是创新并不止于此。两种台架还具有独特的可拆卸 Z 探头。当机器需要调平床时，它会移动到一个角落，从皮套中“快速拉出”一个磁性限位开关。一旦安装好，该探针就成为托架上的最低点，允许托架绕床探测点移动。完成后，探针简单地插回皮套，就可以开始打印了。

Github 上有[wesc 23]的[CroXY 的](https://github.com/wesc23/CroXY)和[Annex _ Engineering]的[的一个变种 K2](https://github.com/Annex-Engineering/Chhogori-K2-Summit-Edition)的完整材料清单，如果你想了解更详细的细节。随着商业 3D 打印机制造商在过去几年中一直处于竞争的最底层，仍然可以看到推动质量和性能的新设计模式的贡献，这是令人兴奋的。更多设计模式贡献，请看【马克·雷霍斯特】[运动学耦合床设计](https://hackaday.com/2018/11/16/expanding-3d-printer-bed-stays-true-under-fire/)。

 [https://www.youtube.com/embed/MTtGYOv85oY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MTtGYOv85oY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

