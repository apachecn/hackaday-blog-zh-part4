# 微小的电阻森林造就了快速而肮脏的自适应光学

> 原文：<https://hackaday.com/2022/07/25/a-tiny-forest-of-resistors-makes-for-quick-and-dirty-adaptive-optics/>

“自适应光学”这个术语听起来应该非常复杂和昂贵。总的来说，控制光学元件属性的能力足够困难，以至于它被保留给像十亿美元的太空望远镜这样的大科学东西。

但这并不意味着没有快速和肮脏的自适应光学系统适合预算有限的实验者，像[这种热变形镜](https://youtu.be/2eiaW2Memqc)。正如[Zachary Tong]解释的那样，这个项目很早以前就开始了，非常简单——一个 4×4 的通孔电阻阵列竖立起来，这些电阻连接在一面镀铝的玻璃盖玻片上。一个 Arduino 和几个移位寄存器可以单独寻址阵列中的 16 个电阻。让电流通过一个电阻会使它变热一点，导致热膨胀和位于阵列顶部的镜子的轻微偏转。控制哪些电阻器变热以及变热的程度应该以可预测的方式导致镜面的变形。

下面的视频展示了[Zach]的一些设置实验。不幸的是，他未能充分展示其潜力——低质量的镜子与他自制的干涉仪不配合。然而，通过加热阵列，他能够使用刻度盘指示器显示镜子在 2 到 3 微米范围内的偏转。光是这一点就很酷了，尤其是考虑到建造成本非常低廉。

至于实际用途，不要太激动。正如[Zach]指出的那样，像这样的热系统可能永远不会像 MEMS 或压电致动器那样快，并且[自适应光学的许多用例对增加的热量反应不佳](https://hackaday.com/2022/05/05/about-as-cold-as-it-gets-the-webb-telescopes-cryocooler/)。但是[用气压](https://hackaday.com/2020/06/27/variable-mirror-changes-shape-under-pressure/)改变镜子的形状是另一回事。

 [https://www.youtube.com/embed/2eiaW2Memqc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2eiaW2Memqc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示。