# 修复 20 世纪 80 年代的惠普 LCZ 流量计

> 原文：<https://hackaday.com/2019/04/07/restoring-an-hp-lcz-meter-from-the-1980s/>

我们非常幸运，不仅因为我们可以以合理的价格轻松获得零件，而且因为我们可以在工作台上拥有负担得起的测试设备。然而事情并不总是这样，[NFM]向我们展示了一个测试设备的大规模拆卸和升级,在那个时代，黑客的工作台只需要一个万用表和一个 10MHz 的示波器就足够了。

Hewlett Packard 4276A LCZ 测量仪是，或者说曾经是，元件测试仪之王。这是一个 19 英寸的机架单元，可以舒适地装满一个货架，它有许多功能和一对红色 LED 显示屏。这种特殊的电表显然经历过更好的日子，需要检查一下内部，只是为了清理连接器和更换老化的电池。

机箱中是一个背板，带有一系列用于 PSU、CPU 和模拟板的边缘连接器。老化的电容器和那些电池被替换，那些边缘连接器被再次清理。CPU 板的中心似乎有一个 Z80，我们确信我们发现了一个 1987 年的日期代码。有很多漂亮的高质量触摸，如个别 7 段数字被嵌入。

该设备的售后选项包括 DC 胶印板，令人难以置信的是，惠普在其手册中公布了其完整的原理图和 PCB 的图片。因此，这是一个简单的过程和快速的 PCB 订购来完成一个现代的复制品，只需几个元件替换和单个电阻来代替惠普专用的封装电阻包。

作为款待，我们得到了一个环场座位，以便进行机器的安装和校准。DC 偏置板给出了错误的电压，他追踪到一个与原始 HP 部件具有不同容差的电压基准。[NFM]对电阻值做了一些调整，能够将电压拉到正确的值。最后，我们看到仪器通过了测试，并演示了陶瓷电容器的电容如何随着接近其工作电压的电压而变化。即使你从来不需要 LCZ 表，或者从来没有见过惠普 4276A，这也应该值得一看。如果你现在有一种冲动，想找一个装满类似宝贝的工作台，看看我们的旧测试设备指南。

 [https://www.youtube.com/embed/kX8WMw0BK7w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kX8WMw0BK7w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

