# 你的植物现在可以自己照顾自己了

> 原文：<https://hackaday.com/2021/03/14/your-plants-can-take-care-of-themselves-now/>

[马赛丽]的人生目标之一是能够坐在家里，看着机器人为他做所有的工作。为了实现这一目标，他已经决定从一些家庭自动化开始，这些自动化将为他照料所有的室内植物。这个项目也是从头开始构建的，是一系列视频的第一部分，这些视频将概述一个完整的开源植物护理机器的构建。

第一个视频从植物的传感器开始。[马赛丽]决定采用基于 STM32 微控制器的完全定制模块，因为商业产品的通信设计很差，还有其他缺陷。这种小板被设计成放置在土壤中，并且具有用于土壤湿度的传感器以及用于可用光量和环境温度的其他传感器。对商用模块的改进包括通过 I2C 进行通信，允许大量模块通过最少的线路进行通信，并以任何需要的方式进行排列。

对于这个构建，所有东西都是开源的，可以在[马赛丽]的 GitHub 页面上获得，包括 PCB 布局和微控制器的代码。我们期待着剩下的视频，他计划在那里布置处理所有这些传感器的中央单元，以及控制它们的定制仪表板。也许还会有一个选项，增加一种方式来[物理地倾听植物传达](https://hackaday.com/2020/10/23/dont-guess-listen-to-your-plants-pleas-for-water/)它们的需求。

 [https://www.youtube.com/embed/ucjUwo17kw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ucjUwo17kw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

