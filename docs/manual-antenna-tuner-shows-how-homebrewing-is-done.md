# 手动天线调谐器显示如何自制

> 原文：<https://hackaday.com/2021/01/15/manual-antenna-tuner-shows-how-homebrewing-is-done/>

如果业余无线电有什么比天线的设计和实现更有魔力的话，我们不知道会是什么。从表面上看，悬挂一大块电线似乎并不复杂，但当你深入细节时，构建有效的天线并将其与手头的工作相匹配可能会非常复杂。

当然，这并不意味着天线主题必须保持完全的神秘，尤其是一旦有人花时间来适当地解释事情。[Charlie Morris (ZL2CTM)]最近用一个简单的天线调谐器做到了这一点，这是一个用来匹配发射机和天线之间阻抗的设备。正如他在下面的第一个视频中解释的那样，他的调谐器设计实际上只是一个惠斯通电桥，其中天线形成一条腿的一半。具有多个抽头和可变电容器的环形变压器形成与高阻抗天线匹配的 LC 电路，在这种情况下是多频带端馈半波，具有收发器预期的标称 50 欧姆负载。一个小仪表和一个二极管检测器指示电桥何时平衡，这意味着收发器看到了正确的负载。

下面的第二个视频展示了调谐器的最终实现；作为一个 QRP 或者低功耗操作的粉丝，[查理]喜欢简单、轻便、易于携带的自制设备，这当然符合要求。[最后一段视频](https://www.youtube.com/watch?v=t9HAvY6n2gw)展示了调谐器在现场的使用，还有一个 [NanoVNA](https://hackaday.com/2019/08/11/nanovna-is-a-50-vector-network-analyzer/) 证明了它能做什么。像往常一样，[查理]抗议说，他不是专家，他只是记录他做了什么，但他总是做得很好，介绍了组件选择所涉及的计算，任何火腿应该能够复制他的构建。

 [https://www.youtube.com/embed/XKzWSsTBjCo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XKzWSsTBjCo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/MZU4xPjGRK0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MZU4xPjGRK0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

