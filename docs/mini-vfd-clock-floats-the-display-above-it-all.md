# 迷你 VFD 时钟使显示器悬浮在它上面

> 原文：<https://hackaday.com/2019/09/26/mini-vfd-clock-floats-the-display-above-it-all/>

正如[sjm4306]所说，“基于过时显示技术的时钟永远不会太多。”我们完全同意，这个单管 VFD 时钟是我们从未见过的。

[sjm4306]选择的时钟所基于的真空荧光显示器是 IV-21，它是一个 8 位 7 段显示器，体积较小。该管是俄罗斯从 80 年代的盈余，因为所有这些显示似乎是。主 PCB 上有一个 ATMega328，一个升压转换器，提供运行 VFD 所需的高电压，一个实时时钟和用于管段的驱动芯片。显像管本身安装在一个聪明的竖卡上，这个竖卡可以将显示屏提升到主印刷电路板上，并将其置于合适的角度以便阅读。【sjm4306】将其设计成模块化；如果您想使用更大的 VFD，您只需制作一个新的竖板 PCB。事实证明，找出 Eagle 通孔间隔的正确方法很难，但他使用电子表格处理三角学并给出每个孔的笛卡尔坐标，从而破解了一个解决方案。相当整洁。下面的视频展示了时钟装配和测试。

出于某种原因，我们真的很喜欢这个时钟的外观——也许是 VFD 的古怪性质，或者是数字的柔和蓝绿色光芒。我们之前已经展示过很多带有奇怪显示的时钟:VFD[大](https://hackaday.com/2019/03/29/a-scratch-built-vfd-clock-with-inner-beauty/)和[小](https://hackaday.com/2019/06/14/stylish-alarm-clock-rocks-a-vfd/)、[仿 NIMO](https://hackaday.com/2018/09/16/this-nearly-nimo-clock-fakes-it-and-makes-it/) 、[解封 LED“灯丝”](https://hackaday.com/2018/09/16/this-nearly-nimo-clock-fakes-it-and-makes-it/)，以及 [Nixies](https://hackaday.com/2019/05/05/web-interface-controls-nixie-tube-clock/) 的 [lots](https://hackaday.com/2018/02/19/the-white-rabbit-nixie-clock/) 和 [lots](https://hackaday.com/2017/01/17/sculptural-nixie-clock-has-shockingly-exposed-design/) 。

 [https://www.youtube.com/embed/7K4XMxCgOIE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7K4XMxCgOIE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

