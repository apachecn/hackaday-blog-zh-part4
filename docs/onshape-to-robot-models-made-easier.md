# 模仿机器人模型变得更容易

> 原文：<https://hackaday.com/2021/02/28/onshape-to-robot-models-made-easier/>

我们生活在一个手机拥有计算能力的时代，这在几十年前是美国国家航空航天局所羡慕的。所以，理论上，我们应该能够模拟任何东西。多亏了[rhoban]，你在 on shape——一个流行的 CAD 工具——中设计的机器人现在[更容易使用几个常见的模拟工具](https://github.com/rhoban/onshape-to-robot/)来模拟。

电子电路很容易模拟，因为我们通常画原理图，电路模拟器可以很容易地捕捉这些原理图。但是为机器人设计模拟物理有点棘手。Gazebo 和 Pybullet 都可以使用 SDF 文件或 URDF。然而，构建这些文件通常是一个独立于实际物理设计的过程，即使您可能使用 CAD 工具进行设计。即使您不使用 OnShape，您也可以导入您喜欢的格式，然后过渡到模拟文件格式，而不必手动重新创建您的设计。你可以在下面的视频中看到作者走过的过程。

这个程序使用 OnShape API，所以你需要一个密钥。示例四足动物看起来是一个很酷的设计。一旦有了正确格式的设计，就可以从模拟的角度使用多种工具来处理它。

我们以前见过 [URDF 为 SolidWorks](https://hackaday.com/2018/05/31/modular-robotics-made-easier-with-ros/) 出口。如果你想有机会玩 Pybullet，试试 [Boston Dynamic 的 Spot 机器人](https://hackaday.com/2020/10/23/the-adorable-robot-spot-now-in-affordable-form/)。

 [https://www.youtube.com/embed/C8oK4uUmbRw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C8oK4uUmbRw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

