# 改进了 JLCPCB 零件的零件搜索

> 原文：<https://hackaday.com/2020/10/11/improved-part-searches-for-jlcpcb-parts/>

Jan Mrázek 发现 jlcpbcomponent parts library 很难导航，于是他自己动手开发了一个开源的参数搜索工具。我们都可能在试图追踪零件的特定味道之前浪费了时间，这个工具有望使这个过程变得更容易。初始化时，它从 [JLCPCB 零件网站](https://jlcpcb.com/parts)下载数据，并为用户提供类别和参数值的典型选择过滤器。你可以自己把它安装在 GitHub 页面上，或者[Jan]给[提供一个到他的网站](https://yaqwsx.github.io/jlcparts/)的链接。

出于好奇，如何从 JLBPCB 站点获取零件信息的细节可以在项目的源代码中找到。我们喜欢分销商提供这种级别的零件详细信息和参数访问，允许其他人以站点设计团队最初没有预想到的方式对零件进行分类和过滤。我们认为这是一个双赢的局面——经销商不能卖设计师找不到的零件。

如果[Jan]的名字听起来耳熟，那应该是。我们之前写过他的几个项目，其中两个也是 PCB 设计工具( [KiCad 板效果图](https://hackaday.com/2017/04/17/a-tool-for-kicad-board-renderings/)和 [KiCad 面板化](https://hackaday.com/2020/04/25/kicad-panelization-made-easy/))。