# 从头开始构建矢量图形机，包括 CRT

> 原文：<https://hackaday.com/2020/12/01/building-a-vector-graphics-machine-from-scratch-including-the-crt/>

多年来，我们已经看到了不少涉及矢量图形的项目，但由[Mark Aren]创建的宇宙飞船游戏尤其吸引了我们的眼球，因为在这个游戏中[他已经着手从头开始构建矢量显示器，而不是简单地使用现成的显示器，如示波器](https://hackaday.io/project/176054-vdm3-vector-drawing-machine-3)。似乎矢量游戏本身还不够有趣，设计驱动 CRT 所需的电子设备的过程在几十年前可能已经司空见惯，但在 2020 年很少有电子爱好者会看到。

在他的文章中，他详细介绍了他选择组件的途径，并给出了 2020 年 it 设计的不同寻常的性质；这是一个迷人的机会，可以看到在 20 世纪 50 年代或 60 年代闻所未闻的部件的工作。他最终选定了一对高压长尾双极晶体管，由单个运算放大器驱动，提供偏转电极所需的差分信号。新旧的混合也需要为 CRT 定制一个插座。与此同时，在游戏方面，ATmega328 通过 DAC 承担重任。他详细介绍了 DAC 的选择，发现有些芯片会产生明显的失真。

总而言之，从各个角度来看，这都是一个令人印象深刻的项目，我们被它深深吸引住了。当然，如果你喜欢矢量图形，[也许有一个更简单的方法](https://hackaday.com/2018/02/03/a-wrencher-on-your-oscilloscope/)。