# 彩弹为你做艺术

> 原文：<https://hackaday.com/2020/02/22/paintbot-does-the-art-for-you/>

数码图像很棒，但真正的手绘作品也有一定的魅力。然而，我们生活在一个数控时代，机器人总是愿意尝试新的东西，如果他们被正确地指导如何去做的话。本着这种精神，[【亚历山大·莱泽】开发了 PaintBot，为他画出美丽的图画。](https://vialps.com/tag/paintbot/)

这个机器人使用铝挤压和步进电机来移动。一个 3D 打印的支架被打印出来，用来放置画笔，这样机器人就可以工作了。[Alexander]用 C#写了一个脚本来解析图像并为“机器人”生成必要的 g 代码。随着时间的推移，这扩展成一个完整的应用程序，有一个图形用户界面和自动颜色变化的规定。需要大量的逻辑，包括清理颜色之间的画笔和正确地合成图像。选择的媒介是帆布上的丙烯酸，在早期用纸做的实验被发现不令人满意之后。

PaintBot 的输出令人印象深刻，单个笔画构成最终图像的方式具有一定的数字质量。[Alexander]也将软件打包并命名为 PaintCam。它分布在 Thingiverse 上，允许任何拥有 3D 打印机的人将它用作机器人画家。

该项目表明，使用 CNC 硬件创建一个漂亮的艺术品是可能的，我们很想看看用神经网络后端做一些艺术解释会有什么效果。如果你建立了这样的系统，一定要让我们知道！休息后的视频。

 [https://www.youtube.com/embed/UKytvy7c3Ew?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UKytvy7c3Ew?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

