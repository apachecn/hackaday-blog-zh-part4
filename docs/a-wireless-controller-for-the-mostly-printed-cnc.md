# 用于大部分印刷数控系统的无线控制器

> 原文：<https://hackaday.com/2020/03/08/a-wireless-controller-for-the-mostly-printed-cnc/>

主要是打印的数控系统(MPCNC)本身就是一个令人印象深刻的项目，允许任何拥有 3D 打印机和一些电气导管的人构建自己的重型数控平台，非常适合布线。定制是 MPCNC 的游戏名称，很少有机器完成后看起来是一样的。但是很少有人会拥有像史蒂夫·克鲁特为他的手机组装的无线手机一样光滑的控制界面。

[![](img/35fa8c83cc06994a36b6335d50a74bcf.png)](https://hackaday.com/wp-content/uploads/2020/03/cncremote_detail.jpg) 在硬件方面，这个项目相当简单。3D 打印外壳内部是 4.3 英寸 Nextion 触摸屏、Mega 2560 PRO 微控制器、nRF24L01 2.4 GHz 收发器和 4000 mAh 3.7 V LiPo 电池，带有适当的充电电路。除了打开和关闭手持设备的物理拨动开关之外，该设备的所有功能都是触摸控制的。对于接收器方面，[Steve]正在使用另一个 nRF24L01 无线电和微控制器对来切换继电器，并来回移动适当的 g 代码命令。

但真正让这个项目大放异彩的是软件。正如你在休息后的视频中看到的，[史蒂夫]在这个控制器的用户界面上做了一个绝对非凡的工作。主题启动屏幕和简洁的图标赋予控制器非常专业的外观，通过在虚拟工作区上点击来推动机器的能力有助于防止触摸界面成为噱头。

[这些年来，我们已经看到了一些令人印象深刻的定制数控控制器](https://hackaday.com/2014/03/14/dagu-the-standalone-cnc-controller/)，但是在使用的大多数现成硬件和令人印象深刻的用户界面之间，我们认为【史蒂夫】创造了一些独特的东西。看起来他暂时对自己保密源代码，但是希望他认为将来发布它是合适的；这样一个项目不仅仅是一次性的创造。

 [https://www.youtube.com/embed/NiKWD2kOsvA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NiKWD2kOsvA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 jeffeb3 的提示。]