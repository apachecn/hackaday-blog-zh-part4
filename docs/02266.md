# 数控你自己的 PCB 与本教程

> 原文：<https://hackaday.com/2019/03/03/cnc-your-own-pcb-with-this-tutorial/>

订购成品印刷电路板变得如此容易，以至于很难证明自己生产是合理的。但有时你真的需要一块板。或者也许你需要很多快速迭代，所以你不能等待邮政服务。[Thomas Sanladerer]展示了他如何用数控机床制作[PCB，并在下面的视频中提供了许多好的建议。](https://www.youtube.com/watch?v=ibZcQLIbets)

他从 Eagle 开始，尽管你可以使用任何创建包。他展示了他改变哪些参数以确保痕迹不会被侵蚀，以及如何进行 CAM 工作以获得制作电路板所需的文件。如果您不使用 Eagle，您将需要推断如何进行类似的更改并获得相同类型的输出。

我们只听过几个人发 Gerber(就像在 Gerber file 里一样)的时候发一个轻 G 音，但是我们还是知道他的意思。GIF 文件我们也有同样的问题。然而，一旦你有 Gebers，你可以加入视频的工作流程大约 5 分钟。

此时，他使用 FlatCAM 将 Gerbers 转换为一个集成了路径和钻孔文件的 g 代码文件。他用了一些小技巧来确保所有的轨迹都被拾取。其他技巧包括通过铣削和安装不同尺寸的钻头来平整扰流板。他也有对齐 Z 轴的想法。

他首先用一些 MDF 废料做了一个模型。当然，最终的电路板使用覆铜 FR-4。有趣的是，该模型充当了董事会的职位指南。即使你没有做一个完整的模型，铣板的轮廓可能是一个好主意。自然，第一次尝试并不成功，他放弃了。他简化了电路板布局，并再次尝试，但效果不佳。然后，他换出了雕刻钻头，他用的是一个合适的端铣刀。这导致了一点需要打磨的边缘，但解决了大多数其他问题。

看起来对于简单的电路板，这种技术还不错，尽管有一些限制。一些痕迹的宽度是错误的，一些环没有钻穿。使用这种铣削工艺在 IC 焊盘之间放置走线似乎也不可靠。

我们已经通过自动调平 FlatCAM 输出避免了【托马斯】遇到的一些问题。我们还看到，铣削仅用于[去除抗蚀剂](https://hackaday.com/2015/06/29/etching-pcbs-with-a-3d-printer/)，然后是传统的酸蚀刻，结果很好。

 [https://www.youtube.com/embed/ibZcQLIbets?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ibZcQLIbets?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

