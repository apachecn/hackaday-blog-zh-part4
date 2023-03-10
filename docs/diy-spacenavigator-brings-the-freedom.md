# DIY 太空航海家带来自由

> 原文：<https://hackaday.com/2022/11/09/diy-spacenavigator-brings-the-freedom/>

想要一个六自由度的 HID。你知道，一个 6 自由度的硬件接口设备。这些是在 3D 空间导航的奇特控制器，用于像计算机辅助设计，或 *Kerbal 空间程序*。虽然我们不能说[Pepijn]的 KSP 上瘾，但我们知道商业上可用的控制器非常昂贵。需要做一些认真的 CAD 工作来证明支出的合理性。[Pepijn]介于两者之间，虽然他无法证明这笔费用的合理性，但他确实有能力设计和 3D 打印自己的。

令人惊奇的是，他分享了 SpaceFox 的设计文件，链接如上。它是 6 个弹簧加载的电位计，支持一个浮动的印刷大旋钮。这些罐子被送入 Arduino Pro 微处理器，该微处理器实时计算旋钮的位置，并将其送入连接的计算机。在计算机端，该项目使用 [`spacenavd`](https://github.com/FreeSpacenav/spacenavd) 驱动程序与各种应用程序接口。

SpaceFox V1 本质上是一个概念验证，只是要求有人来敲掉粗糙的边缘。[Pepijn]甚至包括一个改进的愿望清单，但警告说，他对自己的工作模式感到满意。如果这个项目真的让你的 6DOF 流汁，也许可以尝试做一个改进的版本，并分享这些改进。并让我们知道它！

 [https://www.youtube.com/embed/rLTWWPftyac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rLTWWPftyac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

