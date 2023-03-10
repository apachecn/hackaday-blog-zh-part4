# 柔性电池表向后弯曲工作

> 原文：<https://hackaday.com/2018/11/02/flexible-battery-meter-bends-over-backward-to-work/>

锂离子电池测试仪似乎是一个简单的项目，至少在电学上是如此。但是，当你开始考虑处理大量电池尺寸的物理问题时，事情就变得有点复杂了。当然，你可以 3D 打印适配器和夹具来适应不同的电池，或者你可以欺骗一下，把充电器和测试器电路放在柔性 PCB 上。

也许是卡普顿在说话，但是我们真的很喜欢安德洛卡沃项目的样子。这个想法很简单——与其使用刚性的 FR4 印刷电路板，不如制作一个比待测最大电池稍长的柔性聚酰亚胺薄膜 PCB。两端都有大触点，电路板可以绕过电池读取读数。充电时，电路板另一侧的钕磁铁使充电器与电池保持接触。电路本身是围绕 STM8S003 8 位微控制器和一些分立元件构建的。有一个条形图显示电池电压，涵盖 2.0 至 4.9 伏，还有一个 USB 端口用于充电。这款充电器适用于从 21700 大电池到 14500 小电池的所有产品。在另一个磁铁的帮助下，防止电路板弯曲得太厉害，即使是小巧的 10180 也可以充电。看看下面的视频，里面有一些我们见过的最放松的音乐和最好的 SMD 焊接显微镜照片。

柔性 PCB 是通用的东西。他们不仅能让这样的项目成功，还能[扭来扭去](https://hackaday.com/2018/07/29/flexible-pcb-becomes-the-actuator/)、[游泳](https://hackaday.com/2018/09/14/flexible-pcbs-make-the-fins-of-this-robotic-fish/)，甚至[演奏音乐](https://hackaday.com/2018/09/21/the-diaphragm-is-the-coil-in-these-flexible-pcb-speakers/)。

 [https://www.youtube.com/embed/liu89AIH89Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/liu89AIH89Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

