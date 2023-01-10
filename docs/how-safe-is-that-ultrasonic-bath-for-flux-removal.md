# 超声波浴去除焊剂有多安全？

> 原文：<https://hackaday.com/2019/12/05/how-safe-is-that-ultrasonic-bath-for-flux-removal/>

你如何清除电路板上残留的助焊剂？有很多方法可以着手这项工作，从“为什么麻烦？”用棉签小心翼翼地将异丙醇涂抹在每个关节上。似乎越来越多的人转向超声波清洁器来完成这项工作，不过，有一个很好的理由:只要浸泡你的板，走开，而空化为你工作。

但是用声波吹掉电路板上的焊剂有多安全呢？[SDG 电子]想知道，所以[他进行了一些清洁测试](https://www.youtube.com/watch?v=Li7tAxZPJk0)以弄清事情的真相。从表面上看，将 PCB 浸泡在含水清洗液中似乎是不明智的；毕竟，众所周知水电不能混合。但是假设电路板的所有角落和缝隙都可以在通电前干燥，那么清洗液本身应该没什么问题。超声波清洗的主要问题似乎是声能与电路板上的机械系统耦合，如晶体振荡器或微电子机械系统(MEMS)组件，如加速度计或麦克风。这些部件可能会与超声波产生共振，并在内部爆炸成碎片。

为了测试这一点，[SDG Electronics]用各种潜在的易损组件构建了一个电路板，包括流行的 32.768 kHz 晶体，其频率非常接近清洁器的基频。下面的视频详细介绍了测试前和测试后的情况，但简单来说，所有测试电路都没有出现任何问题。当然，我们没有测试某些 MEMS 麦克风上可能有的带开口的元件，所以要小心。毕竟，我们知道[超声波可以造成伤害](https://hackaday.com/2019/01/07/making-an-ultrasonic-cutter-for-post-processing-tiny-3d-prints/)，如果它能够[悬浮微小的泡沫聚苯乙烯球](https://hackaday.com/2017/01/05/acoustic-levitation-with-a-twist/)，它可能会让你的电路短路。

 [https://www.youtube.com/embed/Li7tAxZPJk0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Li7tAxZPJk0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

