# 透过噪音，看到微小的信号

> 原文：<https://hackaday.com/2018/11/01/cut-through-the-noise-see-tiny-signals/>

示波器是测量各种信号的便利工具，但如果你想测量有周期成分的东西，它尤其有用。现代示波器具有各种内置功能，允许您对数百兆赫的各种信号进行采样，如果您知道该按哪个按钮，查找和测量信号会非常容易。有一些先进的示波器方法甚至超越了最好的示波器的内置功能，[AM] [有关于其中一种方法的教程](https://www.instructables.com/id/Measure-Tiny-Signals-Buried-in-Noise-on-Your-Oscil/)。

这里使用的方法称为相位敏感检测，允许在噪声中发现微小信号，即使噪声的幅度比信号本身大几百倍。通常这是不可能的，但通过将信号移出 DC 范围并赋予其一定的频率成分，然后使用示波器上的第二个通道来测量信号源的频率成分，并在第二个通道上触发示波器，可以将测得信号的相位从噪声中筛选出来，并清晰地显示在屏幕上。

在[AM]的例子中，他使用光电二极管和一个简陋的放大器来测量激光的强度，但即使有了放大器，也很难在噪声中看到信号。通过给激光器的电源添加一个类似 PWM 的信号，然后将其与来自光电二极管的输入信号同步，他可以梳理出他需要的信息。这确实是一个迷人的概念，如果你认为自己是一个示波器高手，这真的是一个你应该放在口袋里的工具。如果你是这种设备的新手，我们也有一些示波器基础知识的入门教程。

 [https://www.youtube.com/embed/kFNf_D7lH6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kFNf_D7lH6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

