# 网络串行终端意味着它总是黑客时间

> 原文：<https://hackaday.com/2022/03/21/web-serial-terminal-means-its-always-hacking-time/>

可以说，你的硬件黑客武器库中最重要的软件之一是一个不错的串行终端仿真器。有很多选择，从经典的命令行工具到更炫的图形选项，它们最终都做了同样的事情:让您轻松地与使用 UART 的小工具进行通信。但是现在你有了一个新的选择——不用安装一个串行终端模拟器，你可以简单地将浏览器指向名副其实的 serialterminal.com。

嗯，也许吧。截至本文撰写之时，它只在 Chrome/Chrome 上运行(推而广之，还有微软 Edge)，所以 Firefox 粉丝将会被冷落，除非 Mozilla [改变他们对整个 Web 串行 API 概念](https://mozilla.github.io/standards-positions/#webserial)的立场。但是假设你*正在*运行适当的浏览器，你将能够用一个简单的界面连接你的串行设备，这个界面应该是任何使用过传统终端软件的人都熟悉的。在 Hackaday Command Center 的一个快速测试中，我们能够在 Linux 上使用 Chrome 毫无问题地调出 Bus Pirate UI。

[![](img/7458568544d6eb73f1b52bdbd7df1083.png)](https://hackaday.com/wp-content/uploads/2022/03/serialterm_detail.png) 这个项目来自 Autodrop3D 的【迈克·莫利纳里】，不出所料，他经常发现自己需要通过 USB 转串口与 3D 打印机控制板对话。由于他最近使用 Chromebook 作为他的主要设备，他认为一个无需离开浏览器就可以使用的快速串行终端模拟器会让他的生活轻松很多。在 HTML、CSS 和 JavaScript 之间只有不到 150 行代码的情况下，他就开始做生意了。添加一个闪亮的新域名，现在我们都有了一个方便的移动黑客工具。

这并不是我们遇到的第一个黑客友好的 Web 串行 API 应用程序。[去年，我们推出了一款与 Logic Green LGT8F328P 微控制器协同工作的网络示波器](https://hackaday.com/2021/02/22/slick-web-oscilloscope-is-ready-in-a-flash-literally/)，以及最近推出的为[浏览器提供 STM32 编译器和调试环境的 Gabuino 平台](https://hackaday.com/2022/01/23/web-centric-gabuino-has-compiler-will-travel/)。

 [https://www.youtube.com/embed/8577GPmvuUQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8577GPmvuUQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

