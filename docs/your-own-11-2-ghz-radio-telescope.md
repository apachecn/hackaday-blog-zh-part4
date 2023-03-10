# 你自己的 11.2 GHz 射电望远镜

> 原文：<https://hackaday.com/2021/02/12/your-own-11-2-ghz-radio-telescope/>

现代生活有其便利之处。通常，这些便利会导致更容易的黑客攻击。一个很好的例子就是卫星电视的兴起及其对业余无线电望远镜的影响。曾几何时，制造一个碟形天线和一个合适的低噪声放大器是一件大事。现在它们是商品零件，你可以在任何地方买到。

使用的天线是一个 1.2 米的主聚焦盘。一些电视碟形天线使用偏移馈电，但这使得它更难用于射电望远镜。除了现成的天线和 RF 组件，AirSpy 软件定义无线电还从天线获得频移输出。在[的后续文章](https://physicsopenlab.org/2020/10/16/a-simple-11-2-ghz-radiotelescope-sw-part/)中有更多关于构建的软件方面的内容。我们喜欢这是一个使用 GNU Radio 的很有内涵的例子。

一点数学预测，望远镜在半功率带宽内大约能看到 1.45 度的天空。由于同轴电缆在 11.2 GHz 时损耗非常大，因此一个转换器正好位于馈电点，将输入信号向下转换到大约 1.4 GHz。然后，信号通过带通滤波器、放大器，传到空中望远镜上。

对于射电望远镜来说，1.2 米并不算大，尽管你可以很容易地看到太阳和月亮的凌日。帖子上说你应该能听到银河系的声音，但是其他的恒星射电源可能太微弱了，不适合这个普通的设备。

这些天我们看到了更多的射电望远镜项目。就算是一个[相对小成立的](https://hackaday.com/2019/11/07/roofing-radio-telescope-sees-the-galaxy/)也能做一些事情。