# FPGA 中的一个临时构建的 RISC-V CPU

> 原文：<https://hackaday.com/2019/11/19/emulating-risc-v-on-an-fpga/>

“RISC 架构将改变一切”，这也是为什么【邵氏】要打造这款很酷的 [RISC-V DIY 复古风格电脑的原因。](https://hackaday.io/project/162397-nedopc-5)

这个项目从另一个黑客的工作中得到灵感，构建了一个 RISC-V 模拟器；在黑客日 [FPGA](https://hackaday.com/2018/10/10/friday-hack-chat-fpga-bootcamp/) 聊天中分享。他更进一步，让它在 UPDuino v2.0 板上运行，该板具有来自 Lattice 的 iCE40 FPGA。

该板通过了他的目标 RISC-V 子集的所有测试，甚至运行了一些泽弗里·RTOS 的例子。他很好地记录了他是如何让代码运行的，以及他到目前为止运行的许多实验。ICEcube2 软件的所有项目文件都已发布。它不是我们在 FPGA 中看到的唯一的 RISC-V CPU，但代码实际上非常清楚，如果你对这些东西感兴趣，值得一读。

我们认为任何对复制他的作品感兴趣的人都可以很容易地这样做，并开始摆弄这个越来越受欢迎的建筑。或者至少让一些 LED 以一种神秘但有意义的方式闪烁。休息后的视频。

 [https://www.youtube.com/embed/lu0mPxgJ4UI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lu0mPxgJ4UI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)