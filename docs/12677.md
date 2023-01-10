# 《2021 年的雷莫蒂肯》//科林·奥弗林扔掉芯片(他们说话了)

> 原文：<https://hackaday.com/2022/02/03/remoticon-2021-colin-oflynn-zaps-chips-and-they-talk/>

Hackaday 的职权范围涵盖了许多令人着迷的领域，其中之一是硬件安全领域，与物理电子硬件一起揭示隐藏在其固件中的内部秘密。科林·奥弗林(Colin O'Flynn)是[chip whisper](https://www.newae.com/chipwhisperer)开源分析和故障注入板的鼻祖，是故障芯片艺术的集大成者。我们很幸运能够欢迎他在去年的 Remoticon 在线会议上发言，现在你可以在休息时间下面观看他的讲话视频。如果你需要学习如何用一次性相机闪光灯之类的东西破解 RSA 加密，这正是你需要的。

本次演讲介绍了信号嗅探和故障注入技术。这是很好的介绍，而不是作为一些高不可攀的魔法，因为他的电源分析演示显示了一个正确的密码攻击的第一个字母明显不同的痕迹，观众只剩下对正在发生的事情的理解，而不是希望在一系列不可理解的灵感。完全控制仪器和目标的学习潜力是显而易见的，随着讨论转移到故障注入，电源毛刺作为一种影响代码执行的技术的介绍将继续。

[![Schematic of an EM injector built from a camera flash.](img/f32054b905a08952288d0854b7a9f1ad.png)](https://hackaday.com/wp-content/uploads/2022/02/em-injection-circuit.jpg)

Schematic of an EM injector built from a camera flash.

他的最后一个技巧是利用电磁脉冲通过电磁注入来观察故障。在这里，他带我们进入了一个科技含量低得多的方向，因为当他向我们展示他的芯片制造商产品时，这一部分的主要内容是展示一个更简单但更便宜的电磁注射器，它是由一次性相机闪光灯的零件制成的。从电子设计的角度来看，有趣的部分来自探针及其触发器，IGBT 用于脉冲安装在 SMA 插头上的小线圈。这里的目标是一个运行重复 RSA 签名测试代码的 Raspberry Pi，即使是更简单的 EM 注射器也能够使它崩溃并提取密钥。他总结了微控制器上相同技术的几个较小的例子，甚至提到相同的技术可以从静电气体打火机这样的初级工具中产生结果。

无论这个演讲是否激励你打开压电灯，自己拼凑一个简单的故障装置，投资一个 ChipWhisper，或者以上都没有，科林的演讲揭示了我们社区的另一种黑暗艺术。

 [https://www.youtube.com/embed/eO-ayS4pbLQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eO-ayS4pbLQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

