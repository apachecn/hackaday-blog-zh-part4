# 一个机器人高尔夫俱乐部(可能)来提高你的游戏

> 原文：<https://hackaday.com/2020/06/11/a-robotic-golf-club-to-possibly-boost-your-game/>

即使对训练有素的球员来说，高尔夫也会令人沮丧，这可能是周六早上说脏话的主要原因之一。为了解决这个全球性的问题，[谢恩·威顿]正在创造终极的~~作弊装置~~[机器人高尔夫球杆](https://www.youtube.com/watch?v=o5Cv9fvajrc&feature=emb_title)，它可以在一次挥杆中消除所有的球杆，并调整所需的距离。

不同的高尔夫球杆主要由它们的杆面倾角来定义，或者球杆面被设计成相对于地面击球的角度，目的是改变起飞角度，从而改变行进的距离。为了消除对不同球杆的需求，[Shane]制作了一个杆头，可以使用旋转编码器设置杆面倾角，并显示在杆身上。然而，建造一个可以承受撞击时产生的 4000 磅力的倾斜机构需要一些巧妙的工程设计。第一次迭代是一个相当令人印象深刻的液压设计，但它需要一个大的液压动力源，系统中产生的压力波每次都会导致头部的活塞爆裂。第二次迭代使用了一个业余爱好伺服系统，结合了机械加工和 SLA 打印部件，但在这种方式下，没有力在冲击时传递到伺服系统，类似于丝杠的工作方式。[Shane]实际上毫无问题地打了整整 18 洞。

球杆的第二个特点是在挥杆过程中根据球杆的速度调整杆面倾角，以将球击出指定的距离。高精度 IMU 用于测量球杆的速度和角度。伺服系统不能瞬间移动，所以它必须根据过去的数据预测撞击速度。不幸的是，没有两个摆幅是完全相同的，这会给系统带来一些误差。

[Shane]将他在 18 洞使用机器人球杆的表现与标准球杆进行了比较，数据显示有所改善，但[Shane]并不认为这都是因为球杆。他希望与 a 500 安打进行更彻底的比较，但他首先想通过旋转球杆的轴来整合一个可以纠正削球和勾手的升级。

像他以前的所有项目一样，[Shane]在解释所有技术细节和所涉及的挑战方面做了令人难以置信的工作，我们期待第二部分。同时，看看他的“特殊”篮球架的[版本 1](https://hackaday.com/2020/04/20/a-basketball-hoop-that-never-lets-you-brick/) 和[版本 2](https://hackaday.com/2020/05/19/robotic-basketball-hoop-v2/) ，以及他用木制钢成型工具制作[钢头鳄鱼](https://hackaday.com/2020/05/07/wooden-sheet-metal-press-tools-make-steel-toecaps/)的尝试。

 [https://www.youtube.com/embed/o5Cv9fvajrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/o5Cv9fvajrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

