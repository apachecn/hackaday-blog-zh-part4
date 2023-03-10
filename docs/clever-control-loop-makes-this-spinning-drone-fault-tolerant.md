# 巧妙的控制回路让这架旋转的无人机具有容错能力

> 原文：<https://hackaday.com/2022/11/09/clever-control-loop-makes-this-spinning-drone-fault-tolerant/>

大多数多旋翼飞机的空气动力学性能和砖头差不多。除非它的所有马达都在转动，控制电子设备在做它们的事情，否则大多数无人机注定会很快变成无人驾驶飞行器，而且通常是以壮观的方式。但是，通过稍微改变一下，有可能使[成为一架多旋翼无人机，即使没有三分之二的电机运转](https://youtu.be/taU7mRTnrtY)也能继续飞行。

我们一直在密切关注[尼克·雷姆]很酷的[旋转无人机项目](https://hackaday.com/2022/07/24/turn-drone-into-a-large-propeller-to-increase-hover-efficiency/)，它基本上避开了刚性机身，而是由三个机翼连接到一个中心轮毂。叶片的总桨距可以通过轮毂中的伺服系统来控制，由于安装在顶部的马达和支柱的推力，整个装置可以旋转并提供升力。我们已经看到[尼克]设法让这个装置升空，悬停是非常简单的。下面的视频涵盖了下一步:获得对末日旋转叶片的俯仰、滚动和偏航控制。

这个问题不简单。首先，[尼克]必须决定一架旋转飞机的前部意味着什么。通过巧妙使用安装在机翼上的 LED 灯条和一些 POV 魔术，他能够直观地指示参考轴。从那里，他能够想出一个方案来改变每个电机的功率，因为它相对于参考轴移动，以正弦或余弦函数调制它，以实现滚动和俯仰控制。这基本上模仿了经典直升机的周期俯仰控制——一种虚拟旋转斜盘。

所有这一切的结果令人印象深刻，尽管有点可怕。[Nick]虽然飞机以 250 转/分的速度旋转，但很明显他控制了飞机，但更酷的是他首先杀死了一个然后两个发动机。它在挣扎，但仍然可控，足以进行颠簸但安全的着陆。

 [https://www.youtube.com/embed/taU7mRTnrtY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/taU7mRTnrtY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

