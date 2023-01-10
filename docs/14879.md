# 将 OSHW 认证的秒表添加到您的工具包中

> 原文：<https://hackaday.com/2022/09/23/add-an-oshw-certified-stopwatch-to-your-toolkit/>

[MakingDevices] [创造了一个简单的秒表](https://www.instructables.com/StopWatch/)，它很好地介绍了表面贴装电子设计和组装。该项目是[开源硬件(OSHW)认证](https://certification.oshwa.org/es000031.html)，与 [Gerbers，KiCAD 文件，软件全部可用](https://github.com/makingdevices/StopWatch)。

从概念上讲，秒表是直接向前的，一行两个四位七段显示器由 PIC18LF14k50 微控制器通过多个 NPN 晶体管驱动。PIC 没有足够的数据线来同时驱动两个显示器，因此使用反相器在两个七段块之间切换。

该电路由 CR2032 纽扣电池持续供电。对于带显示器的正常使用，[MakingDevices]估计可运行 30 小时以上，不带显示器可运行 140 小时以上，但仍在计算时间。空闲时，PIC 的“超低功耗(XLP)”功能使操作窗口估计值远远超出了纽扣电池的自放电。有一个在线串行编程(ICSP)封装，可接受弹簧针 [TC2030-MCP-NL](https://www.tag-connect.com/product/tc2030-mcp-nl-6-pin-no-legs-cable-with-rj12-modular-plug-for-microchip-icd) 适配器来刷新 PIC。

不要让简单性欺骗了你，这是一个记录良好的项目，有关于[设计](https://www.makingdevices.com/SP-Schematics-PCB-design)、[模拟](https://www.makingdevices.com/SP-Simulation)和[电池消耗](https://www.makingdevices.com/SP-Battery-Consumption)的详细帖子。各种视频和迷人的照片展示了从设计、组装、测试到最终验证的整个过程。

很高兴看到这个项目被进一步扩展或改进，也许会有一个可爱的外壳或盒子。

 [https://www.youtube.com/embed/HLl4U4vhF9I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HLl4U4vhF9I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

