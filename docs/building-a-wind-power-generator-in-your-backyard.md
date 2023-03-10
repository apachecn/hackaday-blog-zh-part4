# 在你的后院建造风力发电机

> 原文：<https://hackaday.com/2019/10/05/building-a-wind-power-generator-in-your-backyard/>

对于许多环境爱好者来说，水平轴风力涡轮机(HAWT)——看起来像远处慢慢旋转的风车——是一个非常熟悉的景象。不幸的是，尽管收获可再生能源比依赖天然气和可能耗尽的燃料更可持续，但有相当多的警告使它们更难采用。由于它们面向一个轴，它们需要能够跟踪风，或者权衡最大化能量输出的能力。在湍流和阵风条件下，收获时，HAWTs 也会面临加速疲劳。

![](img/3baaf0f3642d6ecf4c7363048774b37a.png)

垂直轴风力涡轮机(VAWT)的发展解决了其中的几个问题。此外，涡轮机通常更接近地面，齿轮箱更换更简单且更有效。由于涡轮机的尺寸，维护更容易进行，因此通常不需要重型机械来接近现场的关键部件。此外，齿轮箱由于其操作的性质而较少疲劳，并且能够在湍流风中运行，这降低了故障率。

 [![vawt coils](img/6e599611375e5e9a88eda48b95d3e382.png "vawt coils")](https://hackaday.com/2019/10/05/building-a-wind-power-generator-in-your-backyard/vawt-coils/)  [![vawt blade](img/94f6b4d006501ee5410fbe8676d6ae65.png "vawt blade")](https://hackaday.com/2019/10/05/building-a-wind-power-generator-in-your-backyard/vawt-blade/) 

对于一个你可以自己建造的简单版本的 VAWT，蓝花已经公布了一些详细设计布局的机械图纸。风力发电机使用 24 块磁铁、做成线圈的铜线和一块金属板作为主发电机。线圈在静止的板上排列成圆形，而磁铁在移动的圆板上等间距排列。当磁铁经过线圈时，磁通量会感应出电流，电流会随着磁铁旋转速度的加快而增加。

发电机的叶片由蓝色泡沫制成，一根金属棒贯穿其中形成结构。其中三个叶片用三角杆连接到一个中心杆上，中心杆也固定着旋转的磁性板。

![](img/048ad70e3cecf192d1446996cb92eb3b.png)

在[BlueFlower]使用 VAWT 为电池充电的初步试验中，他们能够在升压模式下产生 15W 的最大功率，在 PWM 模式下充电时产生 30-70W 的最大功率。对于一个国产风力发电机来说还不错！

然而，这个设计并不只有优点。虽然 VAWTs 可能更便宜，更灵活，更耐磨，但有一些设计特点会阻止发电机像 HAWTs 一样收集能量。叶片不会同时产生扭矩，一些叶片只是被向前推动。这在叶片旋转时产生了更多的阻力，限制了整个系统的效率。此外，海拔越高，风速越大，因此如果安装在高耸的结构上，VAWTs 的性能会更好。接近地面的振动力也会磨损轴承，导致更多的维护和成本。

 [https://www.youtube.com/embed/DTETK1Clb7w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DTETK1Clb7w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)