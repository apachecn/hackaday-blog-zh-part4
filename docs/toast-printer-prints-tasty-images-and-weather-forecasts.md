# 吐司打印机打印美味的图像和天气预报

> 原文：<https://hackaday.com/2018/12/12/toast-printer-prints-tasty-images-and-weather-forecasts/>

电气工程学位通常侧重于教你有用的东西，比如如何制造实际工作且不会杀死你的电子设备。但这并不意味着你不能在路上玩得开心。这就是康奈尔大学的学生迈克尔·肖(Michael Xiao)和凯蒂·布拉德福德(Katie Bradford)决定用 T.O.A.S.T .做的事情:最初的烤面包艺术解决方案。以防名字没有泄露，这是一个烤面包打印机。用户提供一幅图像和一片面包，T.O.A.S.T .将图像打印到吐司上。或者，打印机可以通过在你的日常面包上打印天气预报来显示天气。

 [https://www.youtube.com/embed/zUwJVrSkh3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zUwJVrSkh3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Xiao]和[Bradford]编写了一个 Raspberry Pi W 来处理大部分繁重的工作，将图像或天气预报转换成 10 乘 10 的矩阵，然后发送到 PIC32。这驱动了两个移动热风枪的马达。为了将矩阵中的 1 变成烤点，马达在面包的一个点上暂停，创造出一个很好的烤点。整个东西被安装在一个激光切割的框架上，带有一个 3D 打印的热风枪支架。不幸的是，没有黄油或果酱分配器，但如果你将它与烤面包机器人结合起来，你可能会得到成品。不过，那可能是研究生水平的建筑。