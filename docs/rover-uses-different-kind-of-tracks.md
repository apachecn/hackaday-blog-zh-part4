# 漫游者使用不同种类的轨道

> 原文：<https://hackaday.com/2021/07/22/rover-uses-different-kind-of-tracks/>

履带式机器人通常需要至少两个轮子才能正常工作。然而，[詹姆斯·布鲁顿]在 20 世纪 40 年代发现了一种奇怪的拖拉机设计，福特森 Rotaped，它在每个履带内只使用一个链轮。作为[詹姆斯]，他围绕旋转概念建造了一个[自平衡机器人。](https://www.youtube.com/watch?v=sC1OkWSt5_I)

Rotaped 使用了六个长的轨道段，长度与车轮的直径大致相同，而不是许多短的轨道段。为了保持车轮上的轨道，在轨道内侧使用了一系列链条或椭圆形框架。

和[詹姆斯]的项目一样，大多数机械零件都是 3D 打印的。为了固定轨道，他在轨道两侧的三个点上拉伸一个橡皮筋环。为了让事情更有趣，他让机器人在轨道上保持平衡。这需要一点 PID 调节才能在没有振荡的情况下工作，因为车轮在轨道内会经历轻微的齿槽效应。车轮由一对带 O-Drive 控制器的无刷电机驱动。平衡由 Arduino Mega 处理，它从连接到 MPU6050 IMU 的 Arduino Pro Mini 读取处理后的位置值。

对于某些应用，这可能是传统走线的可行替代方案，而且减少的零件数量肯定是一个优势。如果有任何想法，请在评论中告诉我们。[詹姆斯]之前建造了另一辆履带式漫游车，它使用了[柔性 3D 打印轨道部分](https://hackaday.com/2020/10/11/modular-rover-platform-rolls-on-3d-printed-flexible-tank-tracks/)。到目前为止，我们见过的最大的 3D 打印履带车是[【伊万·米兰达】的可驾驶坦克](https://hackaday.com/2019/11/02/massive-3d-printed-ridable-tank-boggles-the-mind/)。

 [https://www.youtube.com/embed/sC1OkWSt5_I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sC1OkWSt5_I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

