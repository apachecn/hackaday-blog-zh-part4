# 两个操纵杆通过 VGA 电缆与 FPGA 街机游戏对话

> 原文：<https://hackaday.com/2019/02/11/two-joysticks-talk-to-fpga-arcade-game-over-a-vga-cable/>

我们真的很喜欢以前的黑客出现在举报热线。它展示了硬件黑客社区如何成为一个反馈环，一个黑客引发下一个，如此循环，直到伟大的事情无处不在。这个为 FPGA 吃豆人游戏开发的游戏杆端口是这种创造性转变的一个完美例子。

故事从 *Pano Man* 开始，这个古老的街机游戏版本由【Skip】移植到 Pano Logic FPGA 瘦客户端。[当这个故事](https://hackaday.com/2019/01/11/pac-man-fever-comes-to-the-pano-logic-fpga/)第一次出现时，我们报道了它，它引起了【汤姆·韦伯瑞】的注意，特别是 GitHub 自述文件中暗示可能有更好的方法来处理操纵杆连接的那一段。因此[Tom]接受了挑战，在 VGA 连接器中使用扩展显示识别数据(EDID)电路来支持 Atari 2600 操纵杆。EDID 系统是一个 I2C 总线，所以这项工作需要合适的端口扩展器。[Tom]选择了 MCP23017，这是一款 16 位设备，具有足够的 GPIO 来支持双操纵杆和几个额外的按钮。以前从未设计过 PCB，[Tom]陷入了困境，但很快就想出了一个可行的设计，然后是一个更好的设计，最后是最终版本。下面的视频显示了它与*帕诺曼的行动。*

我们认为[Skip]和[Tom]之间的创意循环非常棒，我们迫不及待地想看到谁会升级。如果你有合适的工具，那么在两条电线上可以填充多少 IO，这是非常惊人的。查看这个 VGA 嗅探工作以了解更多关于 EDID 和 I C 的信息

[https://player.vimeo.com/video/315809161](https://player.vimeo.com/video/315809161)