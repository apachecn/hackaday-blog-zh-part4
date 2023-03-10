# 建立一个多吨动力装载机的乐趣

> 原文：<https://hackaday.com/2021/10/06/building-a-multi-ton-power-loader-for-fun/>

科幻小说中的外骨骼、动力服和铁服多年来一直是许多工程师和工程项目的灵感来源。[Hacksmith Industries]的情况就是如此，自 2019 年 1 月以来，Hackaday 的校友[James Hobson]一直在建造一个大型机械外骨骼，灵感来自《异形》电影中的 P-5000 电动装载机。(视频，嵌在下面。)

与电影版本不同,[Hacksmith]电动装载机不是两足式的，而是建立在小型履带式滑移装载机的底盘上。其现有的液压动力装置也为所有上身液压缸提供动力。上半身保持了电影版的基本外观，由等离子切割钢段制成，在焊接前用标签和插槽系统安装在一起。每个臂有五个自由度，由比例液压阀控制。动力装载机由基于 Raspberry Pi 的工业级控制系统控制，运行 [ROS](https://hackaday.com/2014/01/29/the-robot-operating-system-ros-101/) 。

每个单独的致动器都能够施加足够的力来杀人，因此安全是设计中的一个重要考虑因素。它在几个地方安装了紧急停止按钮，包括一个无线遥控器。ROS 控制器使用弦电位计监控每个气缸的位置，以进行闭环控制，并在执行器越界时触发紧急停止。动力装载机可以由机载飞行员使用一对模拟器飞行控制器操纵杆来控制，或者使用 PS4 控制器远程控制。

[Hacksmith Industries]很清楚这样一个事实，即他们正在建造数吨重的动力负载，用于娱乐和消遣，而不是因为它一定实用或者是商业上可行的产品。然而，其他[外骨骼](https://hackaday.com/2019/01/28/the-cyborgs-among-us-exoskeletons-go-mainstream/)已经证明，它们是一种可行的解决方案，可以减少工业工人的疲劳和受伤风险，以及[在崎岖地形中携带重物](https://hackaday.com/2021/01/06/powered-exoskeletons-in-rough-terrain-an-interesting-aspect-of-the-change-5-recovery-mission/)。

 [https://www.youtube.com/embed/BltPGCDpico?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=327&wmode=transparent](https://www.youtube.com/embed/BltPGCDpico?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=327&wmode=transparent)



 [https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLbncXbXlaNQdNCQQcsvVZx7HTsbLbap2j](https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLbncXbXlaNQdNCQQcsvVZx7HTsbLbap2j)

