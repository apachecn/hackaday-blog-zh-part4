# 用于微小 SMD 零件的 3D 打印碗状进料器

> 原文：<https://hackaday.com/2018/07/22/a-3d-printed-bowl-feeder-for-tiny-smd-parts/>

[Andrzej Laczewski]对于小器件，尤其是 SMD 电阻和电容，有着独到的见解。他没有过多地谈论那个项目，但是从他作为其中一部分建造的原型 [3D 打印碗喂食器](https://bytechlab.com/2018/07/smd-parts-bowl-feeder-prototype/)，我们可以猜测这将是一个非常酷的自动化项目。

碗状进料器是工业自动化中的常见设备，用于将一大堆零件(如螺母和螺栓)一次一个地送到某个流程，通常带有某种定位步骤，以便所有零件都处于正确的位置。他们通过两个轴的振动动作来实现这一点，[Andrzej]通过 3D 打印的 ABS 连杆臂来支撑碗。当碗被定制的缠绕电磁铁拉下时，臂的弹簧力矩会稍微扭曲碗，这样每次碗移动时，零件都会落在稍微不同的位置。对于碗内螺旋上升的浅坡道上的部分，这意味着单列骑到顶部。有趣的是，我们可以看到发送到线圈的信号频率的变化是如何影响馈电的；[Andrzej]在选定专用电路之前，使用了一个函数发生器来寻找最佳点。请看下面的实际操作。

尽管我们想知道振动会对 SMD 元件产生什么影响，但我们对工程设计留下了深刻的印象。尽管如此，我们还是迫不及待地想在一个完成的项目中看到这一点——也许它会像这个 Arduino-fied bowl feeder 一样被集成。

 [https://www.youtube.com/embed/TkSPxxsz-j8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TkSPxxsz-j8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

