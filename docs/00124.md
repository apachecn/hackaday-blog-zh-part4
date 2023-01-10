# 面向大众的开源电源转换器

> 原文：<https://hackaday.com/2018/07/24/open-source-power-converter-for-the-masses/>

GaN 或氮化镓晶体管因其高频和高效率应用而成为新闻焦点。任何对功率转换器领域感兴趣的人都会喜欢西门子的这个[开源项目。该产品名为 SDI TAPAS，是一款基于 GaN FET 的多用途板，片上集成 TMS320F28x 控制器。](https://github.com/SDI-SoftwareDefinedInverter/TAPAS)

快速浏览一下原理图，就会发现有很多东西在工作，比如电流和电压检测芯片，以及设计巧妙的 GaN 功率级，带有常规驱动器。板上有过多的连接器，包括一个用于 Raspberry Pi 的连接器，这是一个额外的奖励。git 存储库附带了示例代码，可以帮助您了解运行 BLDC 汽车公司的示例，并将其连接到 Siemens MindSphere 云平台。

除电机控制外，该平台还可用于多种功能，如电池充电、太阳能采集和无线充电。有一个演示( [PDF](https://github.com/SDI-SoftwareDefinedInverter/TAPAS/blob/master/SDI_TAPAS_introduction.pdf) )可供下载，如果你正在寻找用例，在他们的[社区网站上有许多用户构建项目。](https://tapas.ideas.aha.io/ideas)原理图和电路板设计可以用来制作你自己的，或者你可以向他们要一个样板，他们可能会在他们的社区网站上提供更多。

对于初学者来说，你可能会喜欢这篇关于降压转换器效率的[教程](https://hackaday.com/2018/06/02/buck-converter-efficiency/),感受一下进行这类实验的硬件。