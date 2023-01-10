# 基于 Pi 的光谱仪增加了软件的复杂性

> 原文：<https://hackaday.com/2021/04/23/pi-based-spectrometer-puts-the-complexity-in-the-software/>

摆弄光学足够长的时间，迟早你可能会想要一个分光计。不过，光学仪器是出了名的昂贵，至少对于高质量的仪器来说是如此。但是一个有用的分光计，像[这个 DIY 的基于树莓 Pi 的仪器](https://github.com/leswright1977/PySpectrometer)，不一定要倾家荡产。

这一个是通过[Les Wright]来找我们的，他的[自制激光制造](https://hackaday.com/2020/08/09/how-about-a-nice-cuppa-tea-laser/)我们已经欣赏了一段时间了。[Les]通过保持光学系统超级简单，设法将成本降到最低。仪器的前端只是一个手持式衍射光栅分光镜，就是物理教室里用来演示不同光源光谱特性的那种。把它从分光镜变成分光计需要一个树莓派和一个照相机；相机安装在镜头上，可以看到衍射光栅产生的光谱，相机将数据发送到 Pi，Python 程序将光谱转换为数据。[Les]的软件非常简单，给出了它所看到的光谱数据的图形表示。下面的视频显示了构建过程和校准光谱仪所涉及的内容，以及一些可以轻松探索的更有趣的光谱。

我们欣赏这种设计的简单性和实用性，以及它的适应性。分光镜支架和 Pi cam 支架可以轻松地使用 3D 打印机，而不是使用加工铝，我们还可以看到软件如何适应 PC 和网络摄像头。

 [https://www.youtube.com/embed/T_goVwwxKE4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T_goVwwxKE4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

