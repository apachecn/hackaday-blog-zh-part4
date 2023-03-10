# 手掌中的火

> 原文：<https://hackaday.com/2021/01/29/fire-in-the-palm-of-your-hand/>

自从超级英雄存在以来，他们就激发了黑客项目。对于埃弗雷特·布拉德福德来说，模仿《x 战警》中的角色 Pyro 在过去十年里一直是一个断断续续的项目。他的最新版本 [Pyro 系统 V4](https://www.youtube.com/watch?v=gT04WaCQ3ic) ，集成了相当多的控制电子设备，以在他的手掌中提供相当令人信服的精神控制火的效果。(视频，嵌在下面。)

该系统是一个绑在[Everett]前臂上的电机驱动滑块，它将一个带有集成丁烷燃烧器的旋转末端执行器推到他的手掌中。滑块在 4 毫米的直线轴承上运行，由一个使用电缆的小型齿轮传动 DC 电机驱动。末端执行器装有弹簧以将其推入手掌中，并集成了高压点火电弧发生器电路、喷嘴和电容激活按钮。

丁烷气罐和阀门是从一个小喷灯打火机上拆下来的，阀门由另一个齿轮传动的 DC 马达驱动。阀门致动器、滑动致动器和末端执行器铰链都通过霍尔效应传感器和磁铁集成了位置反馈。铰链中的传感器允许滑块主动校正用户手腕的角度，将末端执行器保持在手掌的中间。

控制电路分为两部分。一个 PIC16 微控制器运行所有的运动控制和位置感测，而连接到小型触摸屏的 PIC18 处理用户界面、控制参数和点火。事实证明，在开发过程中，触摸屏对于控制参数特别有用，无需连接到笔记本电脑。

一些[Everett]以前的版本有更令人印象深刻(和危险)的火焰，但也非常庞大。我们认为这个最新版本在紧凑性和实现令人信服的幻觉方面取得了很好的平衡。

[柯林·福尔泽]是另一个通常与喷火装置联系在一起的名字，但他们有一段被证实的历史，那就是[把他送进医院](https://hackaday.com/2016/03/05/even-colin-furze-gets-burned/)。

 [https://www.youtube.com/embed/gT04WaCQ3ic?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gT04WaCQ3ic?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

