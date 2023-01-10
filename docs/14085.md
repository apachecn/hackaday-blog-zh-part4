# 基于数学的游戏角色

> 原文：<https://hackaday.com/2022/06/30/a-math-based-personality-for-games/>

我们不会因为在 Hackaday 这里专注于硬件而道歉，但这并不意味着我们不会偶尔被一个特别有灵感的比特争论壮举所打动。例如，[t3ssel8r]已经从他的游戏中休息了一段时间来讨论[他的程序动画系统](https://www.youtube.com/watch?v=KPoeNZZ6H4s)及其背后美丽的数学。

有时，游戏会使用程序动画，而不是特定的关键帧。这意味着位置是动态确定的，而不是预先确定的一组位置。开发人员可以使用 IK 或 FK(反向或正向运动学)的组合来求解将末端放置在特定位置的关节的旋转和位置。特别是对于爬行的多肢动物，很容易将一个肢放在地上并保持在那里，直到它太远，选择一个新的位置，并将其移动到那里。这是一段简单的代码，看起来很有说服力。它可以处理复杂的地形和不同肢体位置的情况。

但是，它不能像关键帧那样为运动注入一些生命或个性。[t3ssel8r]介绍了他的基于半隐式欧拉求解器的系统背后的方程和推理。在视频中有一些奇妙的解释，但简短的版本是，他有三个参数来控制系统的频率，阻尼和初始响应。这允许他以某种直观的方式调整行为。一个问题是稳定性；如果时间步长太大，头寸会迅速向外扩张。使用特征值(谁曾想到你会使用这些)来确定最小时间步长允许系统保持稳定，并在需要时采取多个较小的步骤，或者只是暂时限制变化。

如果你正在寻找更多的动画，这个 [blender 插件以一种新的方式](https://hackaday.com/2021/11/30/watch-blender-plugin-make-animated-pcb-traces-and-more/)渲染你的 PCB 轨迹。

 [https://www.youtube.com/embed/KPoeNZZ6H4s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KPoeNZZ6H4s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

