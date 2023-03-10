# 经典凯旋获得现代数字破折号

> 原文：<https://hackaday.com/2021/03/31/classic-triumph-gets-a-modern-digital-dash/>

80 年代，模拟仪表让位于各种花哨的电致发光和 LED 仪表，但这种趋势并没有持续很久。只是在最近十年左右，LCD 数字仪表才真正开始在高档汽车中流行起来。[Josh]正在将现代发动机和传动系统安装到他的经典凯旋 GT6 中，并意识到他必须废弃经典的机械轨距设置。在没有爱上任何现成的东西之后，[他决定从头开始创造自己的解决方案。](https://www.youtube.com/watch?v=ZTHo1FD6wAU)

构建的核心是一个树莓 Pi 4，它通过 CANBUS 与汽车的现代售后 ECU 接口，这要归功于 PiCAN3 附加板。模拟传感器，如油压和冷却液温度传感器，与 Teensy 4.0 微控制器接口，该微控制器具有完成工作所需的模数转换器。显示是通过来自全球速卖通的 12.3 英寸超宽液晶显示器，图形是由 x 下的 Chromium 中运行的自定义 PixiJS 代码生成的。

其结果可与许多其他现代汽车中的数字显示器相媲美，表明[乔希]不仅是一名程序员，还是一名图形设计师。作为奖励，如果他厌倦了设计，改变图形是微不足道的，而不必深入研究汽车的实际硬件。

量表升级在 restomod 项目中很常见；[采取的另一条路线是将传统的机械仪表转换成电子驱动](https://hackaday.com/2020/12/22/v12-corvette-gets-electronic-gauge-mod/)。[如果你正在车库里自己制作一套可爱的仪表，一定要给我们写信！](http://hackaday.com/submit-a-tip)休息后的视频。

 [https://www.youtube.com/embed/ZTHo1FD6wAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZTHo1FD6wAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

