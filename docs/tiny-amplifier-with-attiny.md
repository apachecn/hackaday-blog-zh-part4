# 带附件的微型放大器

> 原文：<https://hackaday.com/2019/02/12/tiny-amplifier-with-attiny/>

小型微控制器能装下相当多的能量。通过正确的代码优化和对可用有限内存的合理使用，即使是小型微控制器也可以做一些他们从未想过要做的事情。然而，即使在预期用途的范围内，这些微型廉价处理器仍有许多令人印象深刻的用途，如[Lukasz]的[音频放大器，在下面嵌入的视频中，它使用了](https://blog.podkalicki.com/attiny13-8bit-mono-class-d-amplifier/)周围最小的 ATtiny 封装之一。

由于 ATtiny 很小，放大器只能实现 8 位分辨率，但由于内部时钟设置和快速 PWM 模式，他可以获得 37.5 kHz 的采样速率。大多数商用放大器的目标频率为 42 kHz 或更高，因此对于有限的硬件来说，这实际上非常接近。它是 D 类放大器的事实也有所帮助，因为它依靠开关和滤波来实现放大。这使得放大器比模拟放大器具有更高的效率，对散热器或过大元件的需求更少。

如果你对开关放大器感兴趣，可以在项目网站上找到[Lukasz]使用的所有代码。他建造这个更多的是出于好奇，为了看看他能从这样一个小的微控制器中得到什么样的品质。对我们来说听起来也不错！不过，如果你对模拟放大器更感兴趣，我们也能帮你搞定。

 [https://www.youtube.com/embed/O8of40tFsD8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O8of40tFsD8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

