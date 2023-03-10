# 单旋翼无人驾驶飞机:推力矢量单旋翼飞机

> 原文：<https://hackaday.com/2018/08/31/single-rotor-drone-a-thrust-vectoring-monocopter/>

我们不确定该怎么称呼这个。它拥有无人机的一般特征，但只有一个旋翼，显然不能用任何标准的多翼机名称来称呼它。直升机？接近，但不完全是，因为转子叶片是固定桨距的。我们现在只讨论“单翼机”，稍后再来讨论这个涵道风扇推力矢量无人机的细节。

无论我们选择如何称呼它——建造者[tesla500]称它为同时乐观和宿命论的“Ikarus”——它确实是独一无二的。单翼机是围绕一个垂直安装在 3D 打印护罩上的 90 毫米电动导管风扇建造的。护罩用作着陆腿和四个伺服系统的安装点，这四个伺服系统在转子垫圈内旋转叶片。叶片偏转气流，并提供推力矢量，使这个小机器的控制。

然而，找到正确的控制方法并不容易。主要由于转子施加的强大回转力，[tesla500]很难让飞行控制器配合。他建造了一个万向试验台来解决这个问题，并最终重写了 LibrePilot 来处理飞船上的独特力，并相应地调整了 PID 回路。看看下面视频中的结果。

当然，一些减少旋翼数量的尝试[比](https://hackaday.com/2018/08/27/the-best-new-quad-is-a-bicopter/)[和其他](https://hackaday.com/2018/06/12/fail-of-the-week-two-rotors-are-not-better-than-four/)效果更好，但是效果很好，我们期待承诺的改进到来。

 [https://www.youtube.com/embed/RMeEh5OUaDs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RMeEh5OUaDs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Larry]和[Danie]的提示！