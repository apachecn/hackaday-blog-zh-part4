# 在改进电源的同时解决接地的秘密

> 原文：<https://hackaday.com/2020/02/04/solving-the-mysteries-of-grounding-while-improving-a-power-supply/>

电气系统中的接地问题和不必要的噪音经常会导致精神错乱。当这些东西中的一个引起的电“小妖精”突然冒出头来时，看起来似乎没有办法解决这种疯狂。然而，当仔细观察时，这些问题会变得更加明显。[在最近的一个视频](https://www.youtube.com/watch?v=VkdtESI6C74)中，【Fesz Electronics】向我们展示了如何通过观察一个小型桌面电源、在 LTSpice 中建模并降低电源输出的噪声来研究这些问题。

虽然这种设置中的所有设备都正确接地，包括电源和示波器，但接地系统的交互方式可能会产生大量噪声。这是通过使用绝缘胶带将电源与大地隔离(不推荐作为长期解决方案)并观察噪声降低而发现的。然而，波纹大幅增加，因此需要更持久的修复。为此，电源在 LTSpice 中建模。这是一个关键的发现:由于电源的所有部分都不是理想的，一些部分的实际电气行为可能会引入噪声。在这种情况下，它是变压器中的非理想电容。

根据该模型，可以通过在输出引线上增加一个更大的电容以及增加其电感来改善该电源。电源中焊接了一个大电容，并增加了一个铁套圈，从而将噪声水平从 100 mV 降至 20mV 左右。虽然还不完美，但对于简单的电源来说，这是一个急需的改进。另一方面，如果你想确保完全消除变压器的电容，你总是可以使用无变压器电源。不过，这也带来了其他风险。

 [https://www.youtube.com/embed/VkdtESI6C74?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VkdtESI6C74?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

