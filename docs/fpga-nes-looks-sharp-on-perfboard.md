# FPGA NES 在 Perfboard 上看起来很锐利

> 原文：<https://hackaday.com/2019/03/18/fpga-nes-looks-sharp-on-perfboard/>

FPGAs 是很棒的东西，里面装满了逻辑单元，可以按照你的意愿重新配置。他们擅长信号处理，任何需要速度的东西，以及重建老式硬件。在这种情况下， [[Jon Thomasson]决定以 perfboard 的形式带回最初的任天堂娱乐系统。](https://hackaday.io/project/77110-spartan-mini-fpga-handheld-nes)

构建使用 Xilinx 的 Spartan 6，Jon 以他自己的开发板设计的形式使用它。NES 内核由来自 Github 的【Brian Bennett】[代码提供。](https://github.com/brianbennett/fpga_nes)游戏通过视差推进器从 SD 卡加载，视差推进器通过串行连接将数据传递给 FPGA。显示在夏普 800×480 LCD 上，NES 的 4:3 视频输出以柱状显示。

该项目在 perfboard 上组装，具有令人愉悦的手持式外形。通过经典 NES 布局中的触觉按钮进行控制。电流消耗约为 400 mA，当使用四节 AA 电池时，运行时间约为 5 小时。

[在](https://hackaday.com/2013/01/23/stuffing-an-nes-into-an-fpga/)之前，我们已经看到古老的 NES 在 FPGA 平台上实现。随着开发板变得越来越便宜，设备变得越来越强大，预计会看到越来越复杂的系统被实现。休息后的视频。

 [https://www.youtube.com/embed/cPJnGYlhwac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cPJnGYlhwac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

