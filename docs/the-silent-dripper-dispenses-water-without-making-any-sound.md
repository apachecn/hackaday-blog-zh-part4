# 无声滴头分配水时不发出任何声音

> 原文：<https://hackaday.com/2021/11/19/the-silent-dripper-dispenses-water-without-making-any-sound/>

工程就是做出符合一系列要求的设计。通常这些都是些无聊的东西，比如成本、功耗、体积、质量或者与现有系统的兼容性。但有时，你必须设计一些你可能从未考虑过的限制。[Devon Bray]的任务是设计一个系统，可以分配单滴水，同时绝对没有噪音。[Devon]的博客详细描述了制作[无声滴头](https://www.esologic.com/silent-dripper/)的过程，这是由[Sara Dittrich]制作的一个名为[的艺术装置【招标间隔](https://www.saradittrich.com/The-Tender-Interval)所需要的。

设计过程从选择合适的泵开始。[离心泵](https://en.wikipedia.org/wiki/Centrifugal_pump)因其平稳、连续的运动而非常安静，但不适合输送少量液体。[另一方面，蠕动泵](https://en.wikipedia.org/wiki/Peristaltic_pump)可以非常精确地产生单滴液体，但它们的夹紧和挤压运动产生的声音要大得多。[Devon]仍然选择了后一种类型，并最终发现用锂润滑脂填充泵送机构可以使其足够安静以达到他的目的。

然后，水泵被安装在一个 3D 打印的支架上，该支架还包含供水管和与外界的电气连接。管道用拉链固定，以防止泵运行时管道移动，泵本身用橡胶减震架与支架隔离。

另一个让泵静音的技巧是电机驱动电路:标准的 PWM 驱动器经常会因为突然切换而导致电机线圈发出呜呜声，所以[Devon]选择了一个 Trinamic SilentStepStick，它可以更加平稳地调节电流。最终的结果是一个滴水器，比一张皱巴巴的薄纸发出的噪音更小，正如你在视频(嵌入下方)中看到的那样，视频也展示了完整的艺术装置。

我们真的很喜欢滴头的机械设计；就我们而言，它本身就应该在画廊中占有一席之地。这也不会是第一个滴水艺术项目；我们已经看过一个雕塑，它显然将水滴悬浮在半空中。

 [https://www.youtube.com/embed/mmAslwyjcbU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mmAslwyjcbU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

