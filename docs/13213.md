# 伺服外科教我们 DIY 编码器植入物

> 原文：<https://hackaday.com/2022/04/03/servo-surgery-teaches-us-diy-encoder-implants/>

今天，我们将讨论[Adam bck strm][如何采用 DS3225 伺服系统并对其进行改造以提高其精度](https://github.com/adamb314/ServoProject)，然后使用这些改造后的伺服系统构建一个高精度机械臂，以展示他的改进程度——位置精度提高了 36 倍。如果这带来了一种*似曾相识*的感觉，那是因为[我们已经在](https://hackaday.com/2021/03/19/robot-arm-achieves-amazing-accuracy-with-just-servos/)之前报道过他的伺服修改，但是现在，还有更多。自上一个视频发布以来的一年时间里，[Adam]已经将它带到了一个新的水平，在下面嵌入的一个新发布的视频[中，向我们展示了修改是如何进行的，以及我们自己如何才能做到这一点。](https://www.youtube.com/watch?v=ECLrLupFW10)

在订购了由[Adam]设计的替换控制器印刷电路板(由您选择的 PCBA 服务机构组装)后，您拆卸了伺服系统，小心地将齿轮箱暂时放在一边。很明显，下一步是去除库存控制板，但从那里开始，你不只是放入新的 PCB 要获得完美的伺服系统，还需要增加额外的传感功能。首先，你必须为控制板打印一个垫片和一个盖子，以及一个新的电机底座。你还必须打印(或者激光切割)两个平面编码盘，一个黑色，一个白色，白色的是偏心的。它只会从这里升级！

这两个圆盘都在马达内部。也就是说，你必须撬开伺服系统的 DC 电机，取出带有刷子的底座，然后插入编码盘。然后，你剪断并锉掉底座的塑料部件，以尽可能多地释放电机底座内的空间，并在释放的空间中添加光学编码器。完成后，将电机、光耦合器和电位计连接焊接到新的控制器 PCB 上，然后将电机重新组装在一起。

在你完成手术后，你必须校准你的伺服系统，为此[Adam]展示了如何正确地机械设置它，提供了你需要运行的代码，甚至是带有控制调整伺服参数的漂亮 GUI 工具——他的固件给了我们比我们从这样的伺服系统中所能期望的更多的能力。所有的旋钮和滑块可用于控制系数，限制和曲线，向我们表明[亚当]真的知道什么是正确的伺服运动。对于这个修改过程的文档、[、解释](https://github.com/adamb314/ServoProject/blob/main/Doc/Theory.md)和工具，我们投入了足够的关注，如果我们自己遵循这些步骤，我们不必担心被落下！

在机器人手臂中，基部的小精度误差会扩大到手臂末端的大误差。如果你渴望的是预算的高准确性，并且你有一点时间来修改股票伺服系统，这种方法可能正是你所需要的，而[亚当]基本上已经为你奠定了所有的基础。上次我们谈到这些伺服修改时，我们的一位评论者提出，这可能是 OpenServo 项目的目标的一个可行的继承者，我们肯定会看到它们来自哪里。如果你想比这更便宜呢？那么，你可以[用“3 美分”的微控制器从垃圾 DC 汽车](https://hackaday.com/2021/12/29/the-three-cent-motor-controller/)制造一个伺服系统。

我们感谢[萨林汉]、[迭德]和[鲍尔德沃]与我们分享这些！

 [https://www.youtube.com/embed/ECLrLupFW10?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ECLrLupFW10?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

