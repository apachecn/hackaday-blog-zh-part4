# 这个 3D 打印机器人真的可以撬锁

> 原文：<https://hackaday.com/2022/05/01/this-3d-printed-robot-can-actually-pick-locks/>

开锁与其说是一门科学，不如说是一门艺术:它可能是 10%的知识和 90%的感觉。只有实践才能教会你对圆柱体施加多大的扭矩，如何感知何时你已经将一个销推得足够远，或者当一个销弹回时是什么感觉。机器人肯定永远无法复制如此微妙的过程，不是吗？

嗯，根据[火花与代码]的[兰斯]的说法，他认为[建造一个开锁机器人将是一个有趣的挑战](https://www.youtube.com/watch?v=bLKxT6O0RQk)。他开始用一个框架来固定挂锁和一个伺服电机来施加扭矩。测压元件测量施加的力的大小。这有助于在每个销子被连续撬开时使锁保持恒定的张力。虽然很慢，但这种方法在手动移动截齿时似乎很有效。

困难的部分是自动选择运动。[Lance]建造了一个由两个电机驱动的智能系统，该系统可以在水平和垂直移动镐的同时保持其笔直。这很难正确工作，但在增加一些额外的夹子来消除丝杠的晃动后，机器人能够开始采摘了。拾取臂内的第二个测压元件将检测每个销上的力的大小，并逐个销地穿过锁。

至少，这是一个想法:事实证明，简单地拖动拨片穿过所有的销子就足以打开锁。一个简单得多的设计可以实现这一点，但没关系:无论如何，为所有这些复杂的运动设计一个机器人是一次很好的学习经历。这也给了[兰斯]一个很好的平台，开始研究一种更先进的机器人，这种机器人可以撬开更高质量的锁，而拖动技术在这种锁中不起作用。

我们以前没有遇到过开锁机器人；或许最接近的对等物是这个 [3D 打印的弹簧枪](https://hackaday.com/2019/07/17/3d-printed-snap-gun-for-automatic-lock-picking/)。如果你对锁的各个方面以及如何使用它们感兴趣，可以看看我们的[物理安全黑客与离经叛道的奥兰姆](https://hackaday.com/2020/06/01/physical-security-hack-chat-with-deviant-ollam/)的聊天。

 [https://www.youtube.com/embed/bLKxT6O0RQk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bLKxT6O0RQk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

