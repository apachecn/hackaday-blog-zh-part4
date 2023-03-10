# 一个很小的火车发车板，就像真的一样

> 原文：<https://hackaday.com/2019/08/05/a-tiny-train-departure-board-just-like-the-real-thing/>

如果你在英国铁路系统旅行，你会熟悉无处不在的橙色点阵出发显示板。它们一眼就能告诉你下几班火车的预计到达时间、开往哪里，底部显示的是当前时间。【克里斯·克罗克-怀特】的灵感来自一条推文，他想把其中一个显示器做成微型，挂在自己的显示器下面。

硬件是一个带有有机发光二极管屏幕的 Raspberry Pi Zero，采用定制的 3D 打印外壳。焊接的 USB 电缆从显示器的 USB 端口获取电源。在软件方面，它是 Balena 云服务的演示工具，从他们的传输 API 中提取数据，但[点阵字体的选择](https://github.com/DanielHartUK/Dot-Matrix-Typeface)是完美的，看起来绝对合适。

对于像这样的项目是否应该需要云服务作为其后端，存在一些问题，当然，它是作为一个示范件，而不是制定离开板的确定方式。然而，它确实为传输数据带来了现成的打包 API，考虑到许多数据源可能是不透明的，这是一个有用的特性。

在大西洋东岸，火车时间显示似乎是一个受欢迎的选择，这里有[另一个英国的](https://hackaday.com/2013/01/08/picture-frame-that-scrapes-train-times-from-the-web/)和[一个爱尔兰的](https://hackaday.com/2016/10/27/train-time-ticker-will-save-your-morning-commute/)。

谢谢你的提示。