# 自动糖果分配器让万圣节的辛苦工作一扫而光

> 原文：<https://hackaday.com/2022/11/10/automatic-candy-dispenser-takes-the-hard-work-out-of-halloween/>

万圣节可能已经过去了，但我们还是忍不住向你展示了[Mellow]的最新项目:[一台自动糖果分发机，让招待不给糖就捣蛋的人不再那么辛苦](https://www.youtube.com/watch?v=ngA6_oVZQao)。这是一个很酷的建筑，可能会成为明年万圣节项目的灵感，或者可能是一个完全不同的场合:想想生日派对或情人节。毕竟，什么时候给你爱的人送糖果不合适呢？

基本概念是一个木制的恐怖脸，当你按下它的鼻子后，它会从嘴里吐出一定量的糖果。分配机构由 3D 打印的机械零件和一根排水管制成。糖果被储存在管子里，每当鼻子被按下时，一个伺服操作的挡板就会释放出一定量的糖果。[Mellow]巧妙地将挡板设计得有些灵活，这样它就不会压碎卡在它和管道之间的任何糖果。

一个 Wemos D1 迷你读出鼻子开关，并驱动糖果分配伺服系统，以及另外两个伺服系统，旋转眼睛左右，以获得额外的视觉效果。最初的想法是让眼睛一直转动，但因为这个机制变得很大声，所以改变了代码，只在分发糖果的过程中转动眼睛。

这些年来，我们已经看到了几款自动糖果分发机的设计，从[一款可以容纳足够一个小城市的糖果的南瓜灯](https://hackaday.com/2020/10/19/stomp-button-receive-candy/)，到[一款更适合作为情人节礼物的漂亮过度设计的机器](https://hackaday.com/2021/02/13/express-your-love-with-candy-and-engineering/)。

 [https://www.youtube.com/embed/ngA6_oVZQao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ngA6_oVZQao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

