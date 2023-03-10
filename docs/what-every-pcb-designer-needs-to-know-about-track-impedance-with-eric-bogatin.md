# 关于 Eric Bogatin 的走线阻抗，每个 PCB 设计人员都需要知道什么

> 原文：<https://hackaday.com/2022/09/12/what-every-pcb-designer-needs-to-know-about-track-impedance-with-eric-bogatin/>

PCB 设计一开始是一件相对容易的事情——你创建一个矩形轮廓，分配一些元件尺寸，运行一些走线，并转储一些 Gerber 文件发送到 fab。然后，随着你越来越有经验，开始尝试更难的电路，接触开关电源、高速数字和低噪声模拟，事情变得越来越困难；我们甚至还没有谈到 RF 或微波设计，从外行的角度来看，事情可能会变得很奇怪。[Robert Feranec]对此类问题并不陌生，他与信号完整性问题的领先专家之一(也是本书作者的个人电子英雄之一)[Prof. Eric Bogatin]合作，深入探讨受控阻抗设计的方式和原因。

![](img/2c5882095f3058a17b9fcf63d66a081d.png)

RG58 cable construction. These usually are found in 50 Ω and less commonly these days 75Ω variants

讨论中一个有趣的部分是为什么 50ω如此普遍？答案首先是历史的。早在 20 世纪 30 年代，无线电应用所需的同轴电缆采用合理的尺寸和聚乙烯绝缘材料，旨在将传输损耗降至最低，阻抗达到 50ω。其次，为成本合理的晶圆厂设计 PCB 走线时，需要权衡功耗和抗扰度。

根据经验，降低阻抗可以提高抗噪性，但会增加功耗，而提高阻抗则相反。您需要在这一点与您所能承受的最终走线宽度、间距和总体布线密度之间进行平衡。

另一个有趣的故事是，当英特尔为图形接口设计高速总线时，创建了一个典型总线结构的仿真，并对物理常数进行了参数化，如走线宽度、电介质厚度、过孔尺寸等，这在低成本 PCB 工厂中是可行的。然后，使用蒙特卡洛模拟运行 400，000 次模拟，他们找到了最佳位置。由于与廉价 fab 设计规则兼容的过孔设计通常会导致过孔特性阻抗非常低，因此建议将走线阻抗从 100ω差分降至 85ω差分，而不是尝试调整过孔几何形状以匹配走线。有趣的东西！

我们承认，这个视频是今年年初制作的，而且*非常*长，但是对于高速数字设计中如此重要的基本概念，我们认为它非常值得您花费时间。我们确实发现了一些有用的花絮！

现在我们已经确定了 PCB 结构，为什么还要绕回来[检查那些电缆](https://hackaday.com/2020/05/24/finding-rf-cable-impedance/)？

 [https://www.youtube.com/embed/U60y4JC0Wxs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U60y4JC0Wxs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

