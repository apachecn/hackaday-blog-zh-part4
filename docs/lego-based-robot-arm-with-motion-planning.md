# 基于乐高的机器人手臂运动规划

> 原文：<https://hackaday.com/2019/07/14/lego-based-robot-arm-with-motion-planning/>

机械臂在工业中有各种各样的应用。无论是焊接汽车，油漆汽车，还是在汽车上安装仪表板，机械臂都可以完成这项工作。然而，你不需要成为一个主要的汽车制造商来试验这项技术。得益于 Arduino 和 ROS，您可以构建自己的机器人，完成正确的运动规划。

运动规划很重要，因为它使机械臂的工作变得更加容易。不是必须手动指定每个关节的旋转，而是用数学来计算所有的事情。末端效应器可以移动，软件将计算出实现最终结果所需的必要运动。这个功能被嵌入到机器人操作系统(ROS)中，并被证明对这个项目很有用。

这种特殊手臂的构造也因其简单而令人印象深刻。它有 7 个自由度，足够玩了。该手臂由乐高技术组件制成，这些组件附加在伺服系统上，并添加了一些 3D 打印组件。这是一种将伺服系统集成到乐高世界的聪明而简单的方法，我们很惊讶我们没有经常看到这种情况。

机械臂仍然是一个活跃的研究领域；甚至有人试图让它们在发生损坏时进行自我纠正。休息后的视频。

[hack adayprize 2019](https://prize.supplyframe.com)主办单位: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip) 

 [https://www.youtube.com/embed/b_GOUNlWADY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/b_GOUNlWADY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

