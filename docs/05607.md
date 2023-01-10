# 电动汽车电机控制器家庭建筑

> 原文：<https://hackaday.com/2020/02/05/an-ev-motor-controller-home-build/>

我们中的许多人都尝试过无刷电机，我们中的一些人会构建自己的控制器，而不是使用现成的部件。这样做有助于理解它们的运行，从而设计出更好的无刷电机供电项目。不过，我们中很少有人能像[etischer]一样，着手为 300V 90kW 牵引电机制造自己的控制器。

高功率无刷电机控制器的棘手部分不在于驱动器，而在于高功率开关装置。他使用了一组 IGBTs，为了驱动它们，他使用了一个更小的工业变频驱动控制器，去掉了自己的输出晶体管。他向我们展示了该系统的一些开发过程，包括展示他通过在晶体管和储能电容之间设置过多电感来放大一组 IGBTs，然后展示他的最终设计。

这是大众十年前首次转换的项目的一部分，作为一系列视频[的一部分，他制作了一个贯穿整个项目](https://www.youtube.com/watch?v=IKR8Or6Im6w)的视频。这是一个电动汽车转换所需部件的迷人分解，以及他在这一过程中遇到的初期困难。

 [https://www.youtube.com/embed/LmqJ6Oruh2A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LmqJ6Oruh2A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/IKR8Or6Im6w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IKR8Or6Im6w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[jafinch78]的提示。