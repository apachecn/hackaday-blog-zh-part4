# 用这个有用的显示器查看土壤湿度

> 原文：<https://hackaday.com/2021/06/18/check-soil-moisture-at-a-glance-with-this-useful-display/>

保持土壤湿润是大多数植物保持快乐的关键。在地铁上把手指伸进脏土里会很痛苦，所以最好有一个工具来代替它。[【Andrew Lamchenko】建造了一个功能强大的土壤湿度监测器，并配备了一个电子墨水显示器，读数一目了然。](https://hackaday.io/project/180373-diy-soil-moisture-sensor-with-e-ink-display)

该设备是围绕 NRF52810 或其他相关的 NRF52 微控制器构建的，这些微控制器运行演出。不是使用现成的传感器来确定土壤条件，而是使用 LMC555CMX 定时器芯片，这是为低功耗设计的经典 555 定时器的变体。结合正确的 PCB 设计，它可以通过检测土壤中的电容变化来充当湿度传感器。该传感器还能够使用 MySensor 协议发送数据，使其能够作为家庭自动化系统的一部分。

土壤通过湿度传感器定期测试，并显示在附带的电子墨水屏幕上。由于电子墨水显示器除了在重写显示器时不需要电力，这允许传感器在不使用大量电池电力的情况下长时间工作。可以检查土壤，更新显示，然后整个系统可以进入睡眠状态，使用少量的电力，直到再次测试土壤的时间。

这是低功耗应用设计的绝佳范例，在这种应用中，器件选择至关重要。我们以前介绍过[Andrew]的项目；他长期以来一直热衷于使用电子墨水显示器来创建持久耐用、低功耗的传感器平台。休息后的视频。

 [https://www.youtube.com/embed/uiuMHfAOONQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uiuMHfAOONQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

