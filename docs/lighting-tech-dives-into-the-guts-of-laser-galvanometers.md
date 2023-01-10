# 照明技术深入激光电流计的内部

> 原文：<https://hackaday.com/2019/06/29/lighting-tech-dives-into-the-guts-of-laser-galvanometers/>

激光灯光秀有一种魔力。看着那束强烈的光来回穿梭，形成各种形状和图案，其中一些甚至是动画，是一件非常美妙的事情。这让我们这些技术爱好者想知道光束是如何被操纵得如此之快的。

当【Zenodilodon】，一个带着深垃圾箱的工作中的音乐会激光技术，潜入[闭环检流计](https://www.youtube.com/watch?v=HIBH55cbfLM)的内部，这是激光表演的核心。检流计与动圈式模拟仪表密切相关，动圈式模拟仪表利用线圈的磁场使指针逆着弹簧力偏转来测量电流。另一方面，激光检流计经过优化，可以非常快速地来回移动轻型镜子，以实现描绘形状所需的偏转。

正如[芝诺]在拆卸一些曾经风光一时的 galvos 时解释的那样，这意味着使用一个被线圈包围的质量非常低的永磁电枢。电枢的一端连接到镜子，另一端连接到传感器，以提供位置反馈。我们发现这部分很吸引人；我们没有想到激光检流计会受益于闭环控制。事实上，一个微小的摆动叶片可以调制来自红外 LED 的光，足以产生一个控制信号，这也是非常酷的。

下面的视频可能有点长，但它是对照明技术日常生活的有趣一瞥。它对我们已经看到的一些激光投影项目进行了一点透视，像[这个巨大的小行星游戏](https://hackaday.com/2017/03/08/light-replaces-electrons-for-giant-vector-graphics-asteroids-game/)。

 [https://www.youtube.com/embed/HIBH55cbfLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HIBH55cbfLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[艾伦·格林]的提示。他在研究他自己的激光检流计项目时发现了它，你绝对应该去看看。