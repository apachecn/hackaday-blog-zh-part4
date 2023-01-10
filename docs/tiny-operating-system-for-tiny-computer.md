# 微型计算机的微型操作系统

> 原文：<https://hackaday.com/2021/06/28/tiny-operating-system-for-tiny-computer/>

在万维网作为事实上获取电子信息的方式变得无处不在之前，有许多其他的在线检索信息的方式。其中最成功的是 Minitel，这是一项法国可视图文服务，从 1980 年一直持续到 2012 年。但是仅仅因为这项服务已经被停用并不意味着它的硬件不能用于像[这种基于 Arduino 的操作系统](http://zardos.fr/)这样的现代版本。([谷歌翻译自法语](https://translate.google.com/translate?hl=&sl=fr&tl=en&u=http%3A%2F%2Fzardos.fr%2F))

这款名为 ZARDOS 的操作系统是在 Arduino MEGA 上运行的，尽管有一个较小的版本可供 Uno 使用。Arduino 通过串行电缆连接到 Minitel 终端。它可以从键盘和 PS/2 鼠标接收输入，并使用同一根电缆在终端屏幕上显示视频。基于 SD 卡的盒式系统具有访问数据的内置功能，这极大地扩展了 Atmel 芯片的有限功能，并且还支持扬声器和可视图文打印机。

尽管该建筑使用了现代微控制器，但它的复古终端还是让我们回想起了 WWW 出现之前的日子。所有的代码都可以在项目网站上找到，任何人都可以构建一个基于 Arduino 的操作系统，尽管构建一个像这样的 Minitel 终端需要一点硬件入侵。无论哪种方式，这都是复兴一些古董法国硬件的好方法，类似于我们看到的将一个硬件转换成 Linux 终端的构建。

感谢[troisieme_type]的提示！