# 用这个 DIY 氢线望远镜探索银河系

> 原文：<https://hackaday.com/2019/09/29/probe-the-galaxy-on-a-shoestring-with-this-diy-hydrogen-line-telescope/>

衬箔泡沫隔热板、碎木料和油漆稀释剂听起来很难像射电天文学家的工具。但是，当与一个 SDR、几个放大器和大量的试错调整相结合时，就有可能[建造自己的氢线射电望远镜](https://www.reddit.com/r/RTLSDR/comments/d7fgz1/hydrogen_line_telescope_made_by_a_hs_teacher_and)并用它来拍摄银河系。

正如名副其实的[ArtichokeHeartAttack]在[非常全面的项目文件](https://docs.google.com/document/d/1_7ZOe1Et_8QTk07bgbTd7LLNqDAtgAjmCS50JM9JRbQ/edit)中解释的那样，当氢原子的质子和电子自旋相对翻转时发出的 1420.4 MHz 特征信号是探索宇宙的重要工具。如果你分析信号的多普勒频移，它不仅能让你看到氢在哪里，还能让你知道它在向哪个方向移动。

但是要做到这一点，你需要一个接收器，从喇叭天线开始收集微弱的信号。高中老师与以前的一个学生合作，用绝缘板和箔带制作了一个金字塔形的喇叭天线。它收集射频信号并将其引导至波导管，波导管由一个矩形涂料稀释剂罐制成，四分之一波长短截线天线伸入其中。来自天线的信号然后通过管道传输到一个便宜的[低噪声放大器(LNA)](https://www.tindie.com/products/gpio/hydrogen-line-pre-filtered-lna-1420-mhz/) 专门为氢气管线设计的，一些前置放大器，一个带通滤波器，最后进入一个 AirSpy SDR。GNURadio 被用来建造分光计，以确定银河系旋转曲线，或银河系相对于其中心距离的旋转速度。

我们以前见过其他[budget H-line SDR receiver build](https://hackaday.com/2017/08/02/cascade-lnas-and-filters-for-radioastronomy-with-an-sdr/)，但这一款仅凭借文档质量就脱颖而出，更不用说它所捕捉到的感染力了。我们希望它能被纳入 STEM 课程计划，并向一些学生展示在有限的预算下可以做些什么。