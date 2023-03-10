# 用电子束光刻技术在硅片上蚀刻出微小的艺术图案

> 原文：<https://hackaday.com/2018/12/13/tiny-art-etched-into-silicon-wafers-with-electron-beam-lithography/>

看起来[山姆·泽洛夫]在他的感恩节假期变得很无聊，他的车库里的事情变得有点奇怪。当然，当你的车库里有一台扫描电子显微镜时，怪异的定义可以包括[尝试电子束光刻](https://www.youtube.com/watch?v=SB94rQtKlKI)，在硅上蚀刻出微小的图像。

你可能会记得[Sam]在他的 DIY 半导体 fab 实验室的 2018 年[hack aday 超级大会演讲](http://hackaday.com/2018/11/19/of-roach-killer-and-rust-remover-sam-zeloofs-garage-made-chips/)，他用这个实验室创造了一个真正的集成电路。该芯片是一个 PMOS 双通道差分放大器，通过光刻技术使用改良的 DLP 投影仪生产。基于光的波长，光刻技术限制了在硅上可以形成多小的特征。

[Sam]现在正在研究使用他的扫描电镜的电子束作为一种数控激光雕刻机来制作更精细的特征。该过程包括用 SU-8 旋涂硅片，SU-8 是一种环氧光刻胶，通常用于紫外光，但也对电子束敏感。他不得不修改他的 SEM，用一个 12 位 DAC 控制 X 轴和 Y 轴偏转，并提供一个定制的光束消隐器。在真空室中有涂层晶片的情况下，标准的激光雕刻软件产生 g 代码来追踪他在抗蚀剂上的测试图像。在丙酮中快速浸泡会使暴露的芯片显影。

[Sam]说这些第一批测试图像不太精致；熊的高度约为 2.5 毫米，线宽约为 10 微米。他的系统目前能够分辨 100 纳米，而商业电子束光刻可以达到 5 纳米左右。他说，在装置中增加一个法拉第笼可能有助于他实现这一目标。听起来像是圣诞假期的项目。

 [https://www.youtube.com/embed/SB94rQtKlKI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SB94rQtKlKI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

