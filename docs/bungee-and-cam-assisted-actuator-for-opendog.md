# 用于开口狗的松紧和凸轮辅助致动器

> 原文：<https://hackaday.com/2021/06/12/bungee-and-cam-assisted-actuator-for-opendog/>

许多步行机器人设计面临的挑战之一是，它们消耗电流只是为了保持直立。詹姆斯·布鲁顿(James Bruton)的一个四足机器人就是这种情况，它的膝盖电机变得太热而无法触摸。添加弹簧来承担一些负载并不像看起来那么简单，所以[詹姆斯]创造了一个[蹦极辅助凸轮机构来完成这项工作](https://www.youtube.com/watch?v=XkELKJA4qpA)。

对于一个普通的弹簧加载杠杆，力与弹簧拉伸的程度成正比，这将要求致动器在腿提升得更高时汲取越来越多的电流。为了使弹簧力在整个运动范围内保持恒定，杠杆臂的长度必须随着膝盖弯曲而不断变短。[詹姆斯]通过在凸轮上拉伸一根橡皮筋来做到这一点。然而，在某些情况下，增加的凸轮体积确实会导致膝盖相互碰撞，但[詹姆斯]计划调整机器人的步态来避免这种情况。他没有抽出时间来实际测量电流消耗的减少，但电机温度已经明显下降，只是在测试运行后稍微有点热。

这些测试是用 [OpenDog V2](https://www.youtube.com/watch?v=ten2T1Pq_z8) 完成的，但是【James】已经在着手 V3 的设计，它将使用 3D 打印的[摆线齿轮箱](https://hackaday.com/2018/08/24/a-peek-at-the-mesmerizing-action-of-a-cycloidal-drive/)。目前，由于[全球零部件短缺](https://hackaday.com/2021/05/24/ask-hackaday-how-is-the-chip-shortage-affecting-you/)，这一建设仍被推迟。

 [https://www.youtube.com/embed/XkELKJA4qpA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XkELKJA4qpA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

