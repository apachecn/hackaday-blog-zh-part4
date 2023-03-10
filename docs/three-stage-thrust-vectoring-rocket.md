# 带有微型飞行计算机的三级推力矢量模型火箭

> 原文：<https://hackaday.com/2021/09/05/three-stage-thrust-vectoring-rocket/>

驾驶推力矢量火箭可能是一项挑战，如果你将多级火箭和一台极简的飞行计算机堆叠在一起，挑战就更大了。但是[乔·巴纳德]不是一个回避这种挑战的人，所以他建造了一个三级主动制导火箭，命名为*史瑞克*T3]。

[乔]以他的推力矢量火箭而闻名，其中一些差一点就能实现完美的[动力着陆](https://hackaday.com/2020/11/27/so-close-to-landing-a-model-rocket-on-its-tail/)。以前的火箭使用了[更大、更复杂的飞行计算机](https://hackaday.com/2020/10/02/advanced-model-rocket-flight-computer-reaching-for-the-stars/)，但是这一次，他想尽可能的小而简约。火箭的每一级都有自己的微型 16×17 毫米飞行计算机和电池。主要组件是运行 Arduino 固件的 SAM21 微控制器、用于高度和方向感测的 IMU 以及用于触发火箭发动机点火器的 FET。它还具有用于推力矢量控制(TVC)的伺服输出，以及用于滚转控制的第三级反作用轮的电机控制输出。为了简单起见，他省略了记录飞行数据的方法，这个决定他后来后悔了。 *Shreeek* 在任何一级上都没有专用的回收系统，而是依靠它的轻重量和高阻力完整着陆

四次发射尝试都没有按计划进行，只有前两级在测试中正常工作，取得了最好的结果。由于缺乏记录的飞行数据，[乔]不得不在每次发射后仅依靠视频片段来诊断问题。即便如此，他诊断问题的经验确实证明了它的价值，并取得了决定性的进步。然而，我们怀疑他未来所有的飞行计算机都将包括数据记录功能。

 [https://www.youtube.com/embed/5TTcbMv5tDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5TTcbMv5tDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢提示[BaldPower]！