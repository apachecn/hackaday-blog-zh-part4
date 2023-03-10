# 制作您自己的技术-HDMI 有机发光二极管显示器

> 原文：<https://hackaday.com/2022/04/01/making-your-own-technically-hdmi-oled-monitor/>

有一天，[mitxela]感到无聊，决定[打造自己的 HDMI 显示器](https://mitxela.com/projects/ddc-oled)——这是非传统的方式。HDMI 有几个高速差分对，但它也有一个 I2C 接口，用于检测显示器的分辨率和发出亮度控制等命令。事实上，I2C 是很多像这样的侧通道的主干——它也是我们连接酷传感器的首选接口之一，在这种情况下，是有机发光二极管显示器！

[mitxela]描述了他的旅程从开始到结束，所有的陷阱和弯路。手里拿着一根损坏的 HDMI 电缆，仔细检查了引脚排列，他想出了如何用 Linux 命令行工具探测 I2C 线，并使用这些工具来验证 HDMI-exposed I2C 总线上的显示器是否被识别。然后，他转向 Python，使用`smbus`绑定为显示器编写了一个简短的库——在偶然发现 SMBus 标准限制导致的 FPS 限制后，他重写了代码，以直接与 I2C 设备节点对话，将 FPS 从 2 提高到 5-10。

由此产生了一个问题——最好的软件路线是什么？他尝试在 HDMI 端口上制作一个定制的 X modeline，从技术上来说，显示器是连接在这个端口上的，但是没有成功。最后，他成功地使用了名为“虚拟监视器”的 Linux 功能，并发现了一个有趣的特性——看不到鼠标光标。事实证明，它们通常是硬件加速的，并由我们的 GPU 覆盖，但在[mitxela]的情况下，GPU 并不参与，所以他也为图片转发代码的[添加了光标支持。](https://github.com/mitxela/ddc-oled)

通过部分刷新，显示可以更快地重新绘制，但这是[mitxela]认为他已经为这次旅程得出了一个满意的结论。这篇文章很值得一读，如果你更擅长看视频，他还制作了一个关于这一切的视频。

14 年前，我们第一次报道了从显示端口[获取 I2C 的能力，并且这个有趣的未被开发的机会不时地出现在黑客的项目中。我们甚至已经看到](https://hackaday.com/2008/05/14/interfacing-your-laptops-onboard-i2c/)[让 I2C 快速脱离 VGA 端口的蓄势待发的突破。](https://hackaday.com/2014/06/18/i2c-from-your-vga-port/)如果你更进一步，用你的 I2C 黑客技术，[你甚至可以剥光 HDCP！](https://hackaday.com/2015/03/12/hdmi-splitter-is-also-a-decrypter/)

我们感谢[sellicott]和[leo60228]与我们分享这些！

 [https://www.youtube.com/embed/8UbVgUFfN8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8UbVgUFfN8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

