# 在这个巧妙的弯曲传感器中，滑动片映射多个弯曲

> 原文：<https://hackaday.com/2020/06/26/slipping-sheets-map-multiple-bends-in-this-ingenious-flex-sensor/>

当想到测量物体弯曲的程度时，很可能会想到应变仪或连杆上的某种编码器。不过，如果[【Fereshteh shah miri】和【Paul H. Dietz】的电容式多弯曲弯曲传感器](https://dl.acm.org/doi/10.1145/3313831.3376269)流行起来，事情可能会简单得多。

这是那些看起来如此明显的想法之一，以至于你不知道为什么它以前没有被尝试过。基本思想是利用弯曲时相互滑动的层状材料的几何形状。想想当你打开一本精装书时，书页是如何展开的，你就会明白了。在 ShArc(“移位弧”)传感器的情况下，书的封面和封底是具有一系列重叠衬垫的柔性 PCB。这些 PCB 之间是一些普通的聚酰亚胺隔离条。传感器的所有条带都固定在一端，所有东西都用一个弹性套管固定在一起。当 ShArc 弯曲时，顶层和底层电极的位置会相对移动，从而改变它们之间的电容。根据电容测量值和每个焊盘的已知位置，微控制器可以很容易地计算出每个点的弯曲半径，并推断出整个条带的曲率。

下面的视频展示了 ShArc 的工作原理，以及该技术的几种应用。作为人手的弯曲传感器的明显用途是最令人印象深刻的——它可以极大地简化[【威尔·科格利】的仿生手控制器](https://hackaday.com/2018/10/18/mechatronic-hand-mimics-human-anatomy-to-achieve-dexterity/)——但这种传感器可以在任何弯曲的系统中工作。另外，在家里做一个看起来很简单。

 <https://hackaday.com/wp-content/uploads/2020/06/paper142vf.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2020/06/paper142vf.mp4](https://hackaday.com/wp-content/uploads/2020/06/paper142vf.mp4)

感谢[Hephaix]的提示。