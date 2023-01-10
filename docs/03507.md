# 电子书阅读器有翻页键，还是不知道

> 原文：<https://hackaday.com/2019/07/04/e-book-reader-gets-page-turn-buttons-is-none-the-wiser/>

大多数电子书阅读器都没有实体翻页按钮。为什么？他们就是不知道。虚拟翻页是通过在屏幕边缘轻敲来完成的。决心减少单手使用的尴尬，【Sagar Vaze】[改装了一款带有两个实体翻页按钮的 Kobo 电子阅读器](https://awildelectron.blogspot.com/2019/07/e-book-reader-page-turn-button-mod.html)作为周末项目。

[Sagar]指出，由于 Kobo 设备的底层操作系统是 Linux，因此可以通过记录然后重放适当的输入事件来伪造对屏幕的触摸(并因此触发翻页)。然而，对于那些愿意稍微改动硬件的人来说，有一个更直接的解决方案。屏幕上的触摸感应是通过红外光束中断系统实现的。沿着屏幕的两边是红外发射器，发射器的对面是接收器。概括地说，当指尖触摸显示器时，至少有两个 IR 光束被阻断，因此可以通过分析 IR 图案是如何变化的来确定指尖的物理位置。

为了欺骗翻页，[Sagar]简单地短路了两个红外发射器:每个轴上一个。IR 的突然闪烁被设备解释为清脆的点击，并且设备顺从地翻页。唯一的问题是两个红外发射器必须同时短路。如果一个在另一个之前短路，器件会忽略它。双极开关可能会做到这一点，但在这方面，零件箱空了，[Sagar]而是使用几个晶体管来完成同样的事情。一个 3D 打印的外壳完善了整个 mod，下面嵌入了一个简短的视频。

 [https://www.youtube.com/embed/t6BWdabE_JU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t6BWdabE_JU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这种模式的好处在于，它不需要与设备的操作系统和高级接口，并且对设备的电池寿命没有影响。顺便说一下，这些设备使用的触摸感应方法让人想起我们自己的【埃利奥特·威廉姆斯】分享的[zForce AIR 触摸传感器](https://hackaday.com/2018/03/06/whats-inside-a-neonode-laser-sensor/)的详细外观。