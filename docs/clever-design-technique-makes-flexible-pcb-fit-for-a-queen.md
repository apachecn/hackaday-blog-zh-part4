# 巧妙的设计技术让柔性 PCB 成为皇后

> 原文：<https://hackaday.com/2022/12/06/clever-design-technique-makes-flexible-pcb-fit-for-a-queen/>

印刷电路板可以是方形、圆形、八边形或任何你想要的形状。但是当涉及到第三维度时，就没有什么选择了:大多数印刷电路板都是扁平而坚硬的。当然，你可以制造柔性印刷电路板，就像你在电子设备中发现的 kapton 背衬的那种，但这些工作起来很复杂。然而，事实证明，你也可以使用普通的 PCB 材料制作柔性电路板:看看[Rehana Al-Soltane]的[柔性皇冠 PCB](https://fab.cba.mit.edu/classes/863.22/Harvard/people/Rehana/week10.html) ，这是她在麻省理工学院[Neil Gershenfeld]的“如何制作(几乎)任何东西”课上做的一个项目。

基本思想是通过铣出几个长槽，用薄片连接两边，在 PCB 上形成弯曲。[Rehana]从[Quentin Bolsée]的[柔性电容传感器项目](https://fabacademy.org/2020/labs/ulb/students/quentin-bolsee/projects/samd11c_flexible_capa/)中获得了这个想法，并将其应用于制作一个带有闪闪发光的 led 的冠状 PCB。皇冠可以弯曲 180 度，实际上可以作为头饰佩戴，用大头针将它夹在佩戴者的头发上。

[Rehana]使用一种叫做 [svg-pcb](https://leomcelroy.com/svg-pcb-website/#/home) 的工具来设计电路板。这是一个开源工具包，让你通过用代码描述来设计 PCB，而不是手工绘制形状。虽然如果你习惯于使用传统的 PCB 设计软件，这可能看起来有点奇怪，但它非常适合制作重复的结构，如表冠中的弯曲部分:只需编写一个`for`循环，让工具生成一个完全相同的插槽阵列。

制造柔性表冠本身也有一些困难，因为在铣削过程完成之前，PCB 就开始弯曲和摆动。事实证明，诀窍是首先在内部切割所有的槽，最后一步只打磨电路板的轮廓。

像这样在 PCB 上增加弯曲看起来是一项很有前途的技术，我们将继续关注这一领域的进一步发展。不过，还有其他方法可以制作可弯曲的电路板:马里兰大学的研究人员使用激光雕刻机制作可折叠的印刷电路板。我们的 [2019 柔性 PCB 竞赛](https://hackaday.com/2019/06/19/these-projects-bent-over-backward-to-win-the-flexible-pcb-contest/)也产生了几个令人印象深刻的实施方案。

 <https://fab.cba.mit.edu/classes/863.22/Harvard/people/Rehaimg/week10/10-blinking.mp4?_=1>

[https://fab.cba.mit.edu/classes/863.22/Harvard/people/Rehaimg/week10/10-blinking.mp4](https://fab.cba.mit.edu/classes/863.22/Harvard/people/Rehaimg/week10/10-blinking.mp4)