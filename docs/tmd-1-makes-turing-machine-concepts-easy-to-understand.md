# TMD-1 使得图灵机的概念易于理解

> 原文：<https://hackaday.com/2020/08/27/tmd-1-makes-turing-machine-concepts-easy-to-understand/>

对于从 20 世纪 30 年代就已经存在并且是计算机科学基础的东西，你会认为图灵机，一种机械计算的抽象，会很容易理解。让抽象的概念变得容易理解是图灵机演示器的目标。

TMD-1 是一个与[迈克尔·盖迪]通常的做法有些不同的项目，通常都是对计算机历史早期的人工制品进行精心制作的再现，如 t [he Minivac 601 trainer](https://hackaday.com/2019/06/17/a-faithful-replica-of-an-early-computer-trainer/) 和[DEC H-500 计算机实验室](https://hackaday.com/2020/06/28/reproduction-1960s-computer-trainer-really-pushes-our-buttons/)。更确切地说，TMD-1 是一种将图灵机的原理具体化的设备。为了表现“磁带”的概念，[Mike]使用了八个伺服控制的翻转瓷砖。机器的“磁头”在概念上沿着磁带移动，其当前位置由亮箭头指示，同时通过轮询伺服位置来读取其上方单元的状态。

在磁带和磁头面板下面是有限状态机，通过它对 TMD-1 进行编程。[Mike]将机器限制为三种状态和四种转变三种符号，每种符号都通过将 3D 打印的瓷砖放置在矩阵上来编程。在印刷过程中，磁体被插入到空腔中；矩阵下方的 PCB 中的霍尔效应传感器读取磁铁的图案，以确定哪些瓦片在哪里。下面的视频展示了 TMD-1 从 0 数到 10 的过程，足以演示图灵机的基础。

很难不评论由 Arduino 运行的图灵机的讽刺性，但鉴于[Mike]的目标是使抽象概念易于理解，利用平台而不是试图用离散逻辑来做这件事是非常合理的。而且你不能和结果争论——TMD-1 第一次让图灵机对我们清晰可见。

 [https://www.youtube.com/embed/AHU15rtGerk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AHU15rtGerk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

