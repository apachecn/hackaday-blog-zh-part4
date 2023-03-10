# 一个方便的电子纸黑客突破板

> 原文：<https://hackaday.com/2022/06/15/a-handy-breakout-board-for-e-paper-hacking/>

如果你关注[Aaron Christophel](相信我们，你应该这样做)，你会知道一段时间以来，他对电子价格标签相当着迷，特别是那些电子纸显示器。不难看出为什么——这些低功耗设备非常适合环境显示，它们的集成无线功能意味着您可以在每个房间放置一个，并通过中央发射机进行更新。

但是市场上有如此多的产品，[Aaron]发现自己在做大量的电子纸逆向工程。这包括在显示器和标签的微控制器之间粘贴一个逻辑分析仪，他发现这是一个相当挑剔的任务。这就是为什么他创造了通用电子纸嗅探器(Universal E-Paper Sniffer)的原因:一种突破性的 PCB，让你可以窥探显示器通信，而不必诉诸令人不快的方法，如刮掉焊接掩模，以手动接入痕迹。

[![](img/e8afbb789c17b46ac0e63d7c97f5255e.png)](https://hackaday.com/wp-content/uploads/2022/06/epaperboard_detail.jpg) 这是一个非常简单的小工具:在两侧，你都有一个用于 24 针 0.5 毫米间距扁平柔性电缆的连接器，这是[Aaron]认为这些显示器最常见的接口，在中间你有一个标准的 2.54 毫米间距接头。电路板上没有其他元件，所有走线都直通另一侧。

添加一些跳线和一个便宜的逻辑分析仪，您就可以嗅探一些 SPI 命令了。休息之后，请观看视频，大致了解一下如何开始搜寻新的显示器。

用于 breakout 的 Gerber 文件是免费的，或者您可以选择通过 PCBWay 购买一个装配式电路板，以向[Aaron]支付部分销售价格。无论你如何得到一个，我们认为如果你发现自己被价格标签黑客 bug 所困扰，这将是一个方便的小工具。

 [https://www.youtube.com/embed/gGNzAxeF2o4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gGNzAxeF2o4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

