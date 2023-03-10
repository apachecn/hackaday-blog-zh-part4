# 为库存摩托车添加升级

> 原文：<https://hackaday.com/2018/09/11/adding-upgrades-to-a-stock-motorcycle/>

在当今世界，从汽车到手机到冰箱，所有东西都在进行无线固件升级，各种东西的制造商锁定软件功能并强迫你为升级付费是很常见的。即使所有型号的硬件都是一样的，如果您想解锁任何额外的东西，您仍然可以使用钩子。而且，[铃木似乎也在追随这一趋势](https://www.youtube.com/watch?v=plvlS--2Huw)，正如【Sebastian】在打开他的 2011 款 Vstrom 摩托车时发现的那样。

这辆自行车缺少的主要特征是一个档位指示器。尽管变速箱中所有的硬件都可用，并且 ECU 能够知道当前使用的档位，但仪表组上没有指示器。通过使用 Arduino 与 OBD 阅读工具(现在甚至摩托车[也使用 OBD](https://hackaday.com/2017/01/04/on-board-diagnostics/))配对，[Sebastian]能够将 LED 环连接到仪表组，以显示他骑行时的当前档位。

构建非常专业，并且很好地融入了仪表组，甚至我们一开始也很难发现它。虽然这一功能可能需要铃木仪表组上的一些额外照明才能提供这一功能，但我们已经看到了设备中的[其他“缺失”功能，只需很少的努力就可以解锁。](https://hackaday.com/2014/08/05/hardware-security-and-a-dmca-takedown-notice/comment-page-2/)

 [https://www.youtube.com/embed/plvlS--2Huw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/plvlS--2Huw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

