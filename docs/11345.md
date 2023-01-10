# 特斯拉门把手改进

> 原文：<https://hackaday.com/2021/09/16/tesla-door-handle-improvements/>

汽车工程师和前特斯拉雇员[SuperfastMatt] [看看臭名昭著的特斯拉门把手设计，以及这些年来它是如何改变的](https://www.youtube.com/watch?v=Bea4FS-zDzc)(见休息下方的视频)。最初的手柄设计由许多易出故障的活动部件、开关和电线组成。严格来说，门把手位于汽车内部的外侧。虽然它避免了直接暴露在自然环境中，但它仍然会经历极端的温度、湿度和冷凝。手柄很容易出故障，于是出现了一个家庭手工业来提供改进的零件和替换品。

多年来，特斯拉进行了各种改进，最终推出了[Matt]在本视频中回顾的最新版本。几乎所有的故障点都已消除，除了手柄本身，唯一的移动部件是一个磁性传感器来检测手柄的运动(以前这是通过微动开关来检测的)。[Matt]独立打开控制模块，发现一个恩智浦可编程角度传感器( [KMA215](https://www.nxp.com/products/sensors/magnetic-sensors/angular-position-sensors/programmable-angle-sensor-with-sae-j2716-sent:KMA215) )。这种一体化传感器可以检测磁场的角度，并通过汽车通信总线进行报告，这种总线在过去十年中越来越常见:[单边半字节传输](https://en.wikipedia.org/wiki/SENT_(protocol)) (SENT)又名 SAE J2716。SENT 是一种低成本、仅传输协议，专为传感器向 ECU 发送数据而设计。看看[Matt]在示波器上解码它和视频中的 Raspberry Pi——乍看起来非常简单。

我们同意[Matt]的结论，即除了是否需要可伸缩门把手的问题之外，门把手设计在最新版本中得到了显著改进。如果你想了解更多关于 SENT 的知识，这里有一个由 IDT(现在的 Renasas)应用工程师蒂姆·怀特撰写的[教程。这并不是[Matt]第一次接触特斯拉门把手——](https://www.renesas.com/us/en/document/whp/tutorial-digital-sent-interface-zssc416xzssc417x)[早在 2012 年，我们就报道过他的项目](https://hackaday.com/2012/12/20/tesla-model-s-handle-dispenses-beer-hides-when-done/)，用它来分发啤酒。感谢[JohnU]发送此提示。

 [https://www.youtube.com/embed/Bea4FS-zDzc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Bea4FS-zDzc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

