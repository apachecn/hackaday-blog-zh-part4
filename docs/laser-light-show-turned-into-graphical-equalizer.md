# 激光灯光秀变成了图形均衡器

> 原文：<https://hackaday.com/2019/02/13/laser-light-show-turned-into-graphical-equalizer/>

摇滚音乐会期间激光表演的黄金标准是平克·弗洛伊德，表演以视觉效果和优秀的音乐而闻名。并不是所有人都有必要的资金来制作如此宏大的声光挂毯，但只要有一点点硬件，我们就能得到接近的东西。[詹姆斯]的最新项目是这样的:他最近建造了一个[激光图形均衡器](http://www.xrobots.co.uk/laser-projector-graphiceq/)，可以在他的乐队演奏时使用。

为了创造平衡带的激光线，[詹姆斯]使用了一系列安装在旋转轴上的镜子。当激光投射到旋转的镜子上时，会产生一条线。从那里，他需要一种方法来管理七条线的高度。他使用了一系列带有伺服电机的护罩，可以将激光线关闭到适当的高度。

项目的最后一部分是完成编程。这个项目的大脑是一个 MSGEQ7，它接收音频输入信号，并将其分成七个频率用于均衡器。七个频率中的每一个都被馈送到七个伺服控制快门中的一个，该快门使用 Arduino 控制每条激光线的高度。这是一个伟大的项目，而且[詹姆斯]可能正在将激光用于其他有趣的音乐目的。

 [https://www.youtube.com/embed/7u3TRbWFYgk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7u3TRbWFYgk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

