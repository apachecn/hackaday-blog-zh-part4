# 现场黑客和 MIDI 键盘手

> 原文：<https://hackaday.com/2019/03/02/live-hacking-and-a-midi-keytar/>

我们想不出你会在哪里买到一个新的，便宜的 MIDI keytar，它只是一个键盘和一个带有一些音高和调制轮或色带控制器的手柄。这是一种在 90 年代左右消亡的格式。是的，摇滚乐队控制器是存在的，但我的观点仍然有效。事实上，你能得到的最便宜、简单的 MIDI keytar 是 Alesis Vortex Wireless 2 Keytar，但手柄上的按钮没有任何意义。Wii 和 Kinect 黑客名声的[marcan]注意到了。(YouTube，下面嵌入。)

逆向工程是一个研究项目，所有的研究项目都从查看文档开始。当谈到消费电子产品时，最好的资源是一家公司被要求提交给 FCC 的文件(大声喊到 [FCC.io](http://fcc.io/) )，这些文件给了【marcan】用户手册，以及 keytar 内部的照片。“系统更新下载”文件存在于 Alesis 服务器上，这就是你对 keytar 进行逆向工程所需要的全部内容。

第一步是从下载软件更新时出现在桌面上的任何软件包中提取实际的设备固件。这对于 7zip 来说是一项简单的工作，在查看了固件的二进制转储之后，[marcan]发现这是针对 STM 芯片的。有了芯片的数据表，[marcan]就有了固件的切入点，一些值，真正的硬件黑客行动就开始了。所有这些都是和艾达一起完成的。

这是一个五小时的黑客会议，交叉引用 MIDI 规范和该规范开发三十年后构建的微控制器。与处理 keytar 手柄上的按钮相比，仅仅是找到一点代码就已经是一项惊人的工作了，而且当补丁固件上传后，这项工作会变得更好。如果你想“学习黑客技术”，就像我们的提示热线上的许多提交者想做的那样，这是你需要关注的。谢谢你的提示。

 [https://www.youtube.com/embed/OHYq3zNR1yo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OHYq3zNR1yo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

