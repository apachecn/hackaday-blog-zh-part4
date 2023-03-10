# 进行一次 3D 打印的无刷电机演示

> 原文：<https://hackaday.com/2020/05/18/take-a-3d-printed-brushless-motor-demo-for-a-spin/>

用回形针或电线制作某种马达曾经是初中物理课的主要内容。线圈产生磁场，使转子运动。在移动的过程中，将线圈连接到电路其余部分的电刷将反转其极性，并改变磁场以保持转子转动。然而，无刷电机的工作方式不同。磁场的变化来自驱动控制器，而不是刷子。如果你想[建立那个模型](https://www.instructables.com/id/3D-Printed-Brushless-Motor/)，【Rishit】已经满足你了。你可以在下面的视频中看到他的 3D 打印模型无刷电机运行。

通常，你有一个微控制器来决定如何驱动电磁铁。然而，这个模型比那个更简单。有两个永久磁铁安装在轴上。一个磁铁闭合簧片开关给线圈通电，另一个磁铁处于线圈吸引它的位置，切断电流。随着轴的转动，最终第二个磁铁将触发簧片开关，线圈将吸引第一个磁铁。这个过程一遍又一遍地重复。

诚然，一个真正的无刷电机可能有更多的线圈，并可能逆转磁场而不是关闭它，但这个简单的演示器显示了一个没有电刷的电机如何旋转的基本想法。簧片开关(或霍尔效应传感器)也提供转速反馈，您可以使用正确的控制电路或软件来控制电机的速度。3D 打印的零件外观整洁。你确实需要一个轴承和一些电线。还有一个可选的开/关开关。

如果你手边没有轴承，我们已经看到[坐立不安旋转器](https://hackaday.com/2017/12/28/fidget-spinner-becomes-a-brushless-motor-remains-useless/)用于这种事情。既然它们已经成为历史时尚，你可以非常便宜地买到它们。如果你想看看真正的无刷电机，你可以在[看到一个正在重建的](https://hackaday.com/2017/11/15/rewire-your-own-brushless-motors/)。你可能也有兴趣看看真正的电动 T4。

 [https://www.youtube.com/embed/hx0AActapEs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hx0AActapEs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

