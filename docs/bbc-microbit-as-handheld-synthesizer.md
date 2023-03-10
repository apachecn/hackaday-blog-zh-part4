# BBC Micro:Bit 作为手持合成器

> 原文：<https://hackaday.com/2022/12/17/bbc-microbit-as-handheld-synthesizer/>

BBC Micro:bit 虽然在我们的社区中不像其他微控制器开发板那样受欢迎，但它有一些怪癖，可以使它成为一个比 Arduino 更有趣的硬件来构建项目。[Turi]注意到了这些独特的特性，并认定它是在上构建合成器的[完美平台。](https://turiscandurra.com/2022/04/ts-det1-microbit-keypad-synth-with-detuning/)

Micro:bit 包括两个使这个项目成功的重要元素:LED 矩阵和陀螺仪传感器。[Turi]为输入构建了一个 5×5 按钮矩阵，并将每个按钮与一个二极管配对，这消除了错误输入的问题。陀螺仪传感器用于解谐，它根据设备的方向将任何生成的声音的音高改变设定的量。它还包括一个无源低通滤波器，使声音更加悦耳，尤其是对该机的年轻玩家而言。他在他的 GitHub 页面上发布了源代码，供有兴趣的人使用。

虽然这是[Turi]的一个一次性项目，但他指出，使用 MicroPython 而不是 C 编写程序导致了许多不必要的复杂性，而 C 允许的更大的控制能力将使一些额外的功能更容易实现。尽管如此，这仍然是一个有趣的项目，它真正展示了这种板的独特功能，[很像我们在夏天报道的这个小型相扑机器人](https://hackaday.com/2021/08/21/pint-sized-sumo-robot-is-adorable-accessible-and-totally-awesome/)。

 [https://www.youtube.com/embed/FmPN0WHgj7s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FmPN0WHgj7s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

