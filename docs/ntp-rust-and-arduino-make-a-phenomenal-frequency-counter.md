# NTP、Rust 和 Arduino 构成了一个非凡的频率计数器

> 原文：<https://hackaday.com/2021/11/17/ntp-rust-and-arduino-make-a-phenomenal-frequency-counter/>

使微控制器像频率计数器一样工作是一项相对简单的任务，包括测量对多个脉冲进行计数的时间周期。然而，最大频率受限于微控制器时钟速度的一部分，并且最终仪器的精度取决于时钟晶体的精度，因此它几乎不会产生最好的频率计数器。这是[FrankBuss]用基于 Arduino 的计数器处理的事情，它将计时问题卸载到主机 PC，并因此声称原子精度，因为它的时钟通过 NTP 绑定到主源。Rust code PC-side 提供连续读数，其准确度随着计数时间的延长而提高。所示示例在读取 1 MHz 源数小时后达到十亿分之 20。

很明显，这不是最方便的频率计数器，但是我们可以看到，它可以用于任何想要监控源长期稳定性的人，甚至可以与某种反馈一起使用，通过使用适当的预分频器，根据 NTP 时钟来调整 RF 源。虽然它真正的使命可能不在于测量，而在于校准另一台仪器，一旦它稳定下来，就可以进行调整以匹配它的读数。肯定没有更便宜的方法来满足你内心的频率标准狂热。