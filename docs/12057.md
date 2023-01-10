# 计算器的魅力:利维爱计算器！

> 原文：<https://hackaday.com/2021/11/28/the-calculator-charm-calculatorium-leviosa/>

你有没有试过像挥魔杖一样挥挥手，召唤一个计算器？我们认为不会，因为你这样做可能看起来有点傻。除非你有[【安德烈的】很酷的手势控制计算器](https://www.hackster.io/andrei-mitrofan/no-touch-gesture-calculator-40e7d4)。[Andrei]认为在他的研究实验室使用计算器会有所帮助，而不必脱下手套，结果非常酷。

他的硬件包括一个袖珍猎犬、一个有机发光二极管和一个 MPU6050 惯性测量单元，使用加速度计和陀螺仪捕捉他的手部动作。硬件非常简单，所以这个项目的美妙之处在于它的机器学习实现。

[Andrei]首先捕获了一些示例数据集，通过为每个数字 0-9 重新创建手势来训练他的算法，并记录由此产生的加速度计和陀螺仪输出。他首先用小波变换处理了数据。这种转变的目的是双重的。首先，转换使他能够减少数据集中的样本数量，同时保留加速度计和陀螺仪信号的形状，这是机器学习分类中的关键特征。第二，他能够增加用于分类的特征的数量，因为小波变换产生了近似值和细节系数，这两者都可以被馈送到算法中。

因为他有一个小数据集，所以他使用分层洗牌分裂技术，而不是通常更适合大数据集的测试序列分裂方法。分层洗牌分割确保每个手势的训练和测试样本数量大致相同。他还非常注意优化他的模型，以便在 PocketBeagle 这样的便携式处理器上运行。他花了一些时间来优化他的算法的参数，并最终使用 TensorFlow 内置的“TFLiteConverter”函数将他的模型转换为 TensorFlowLite 模型。

最后，在真正的开源方式中，[他的所有代码都可以在 GitHub](https://github.com/mitro99/ENGI301/tree/main/project_01) 上获得，所以你可以自己尝试一下。[利维爱！](https://hackaday.com/2020/04/05/harry-potter-wand-hack-makes-magic-real/)

 [https://www.youtube.com/embed/agfddy2tojQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/agfddy2tojQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

