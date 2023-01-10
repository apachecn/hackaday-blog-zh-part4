# OpenDog:添加力敏感脚

> 原文：<https://hackaday.com/2020/01/04/opendog-adding-force-sensitive-feet/>

[James Bruton] OpenDog 仍然是我们在 Hackaday 上看到的最令人印象深刻的自制机器人项目之一，它是一份不断送出的礼物。这一次，他致力于为 OpenDog 的腿部增加[力感能力](https://www.youtube.com/watch?v=-asp12aovNs)，以实现更动态的运动控制。

腿中的致动器是三相外转子电机，通过皮带驱动滚珠丝杠。这种配置是不可反向驱动的，这意味着当外力作用时腿不能移动，这可能导致机械故障。他用其他机器人测试了其他可反向驱动的腿配置，但不想完全重建 OpenDog。[詹姆斯]采用的解决方案是重新设计一只带有内置开关的脚，以确认脚是否接触地面，并在底部腿段的中间连接一个测压元件。称重传感器通过螺栓牢固地固定在腿段上，这使得它可以在腿承受负载时进行感应，而不会损坏称重传感器本身。

不幸的是，OpenDog 的主要 Teensy 3.6 控制器上的所有串行端口都已被使用，因此他将来自称重传感器的信号转换为 PWM，以允许它由正常的 GPIO 引脚读取。这在隔离时工作良好，但当[James]打开电机时，来自负载传感器的 PWM 信号被干扰淹没，使其不可读。为了解决这个问题，他想实现一个 CAN 总线，这将允许更多的输入和输出，并有望解决干扰问题。然而，[James]没有使用 CAN 协议的经验，所以学习使用它将是一个独立的项目。

OpenDog 已经变成了一个非常漫长、耗时的项目，[James]说从这个项目中学到的经验对许多其他项目来说是无价的。这是我们处理任何事情都要记住的。选择那些获得的经验和/或发展的关系本身是值得的项目，即使项目在传统意义上失败了。这样你永远不会真的输。

 [https://www.youtube.com/embed/-asp12aovNs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-asp12aovNs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

