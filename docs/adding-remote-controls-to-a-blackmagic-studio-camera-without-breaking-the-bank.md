# 为 Blackmagic Studio 相机添加遥控器，而无需倾家荡产

> 原文：<https://hackaday.com/2021/05/22/adding-remote-controls-to-a-blackmagic-studio-camera-without-breaking-the-bank/>

当一个人最终拥有了一台 4K 工作室相机，却没有必要的硬件和软件来遥控它时，该怎么办？当[格伦·艾金斯]在这种情况下结束时，他在这里采取了合理的选择，[开发了他自己的旋钮式遥控器](https://bikerglen.com/blog/usb-knobs-that-double-as-a-blackmagic-remote/)来调整曝光和聚焦在黑魔法设计的[微型摄影棚摄像机 4K](https://www.blackmagicdesign.com/products/blackmagicmicrostudiocamera4k/techspecs) 上。如果没有远程控制选项，唯一的调整选项是通过相机本身上复杂的小按钮，这在使用该相机的网络摄像头期间不会是一个有趣的体验。

该摄像机通常通过 SDI 输入上的控制通道进行控制，SDI 输入还处理摄像机的视频输出。对于较大的安装，通常使用专有的 ATEM 软件，还有一个 99 美元的 Arduino 扩展板，显然很少库存。SDI 不是一个选项，第二个选项是 LANC，它遇到了与专有协议和非常昂贵的硬件几乎相同的问题。

在三号门后面是更奇怪的双叶 S.BUS 协议的控制选项。最初是为遥控无线电控制的飞机和类似的遥控系统而创建的，这里的想法似乎是，这种工作室相机也可以用于已经有 S.BUS 接收器的系统，如大型无人机。

这种 S.BUS 协议已经逆向工程了一段时间，因此创建一个基于 MCU 的电路板是一个相当简单的过程，板上有许多编码器旋钮，可以映射到相机上的特定调整。【格伦】的劳动成果可以在 GitHub 上找到[。](https://github.com/bikerglen/usb-knob-box-bmd-remote)

**主图:**完成的黑魔法设计相机旋钮盒。(鸣谢:格伦·阿金斯)