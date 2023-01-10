# WiFi 黑客咖啡先生

> 原文：<https://hackaday.com/2020/09/29/wifi-hacking-mr-coffee/>

你在一个星期天醒来，从床上爬起来，走向早晨的中心，一个帮助你开始新一天的神奇设备:咖啡机。你打开配套的 app，因为 2020 年万物都有 app，选了一大杯多泡沫的拿铁。当你打开浏览器查看黑客日时，机器会发出哔哔声。然后内置的研磨机转动到 100，牛奶起泡器开始旋转，机器开始喷水。慌乱中，你看着显示屏上的错误代码，却看到一条信息，指示你将 75 美元存入一个比特币钱包，以免你 300 美元的机器变成一个门挡。

尽管看起来很奇怪，但正如 Avast 威胁实验室的 Martin Hron 所证明的那样，这已经成为一种非常现实的可能性。事实上，他可以让你的现代玛奇朵(macchiato)咖啡机做到这一点，而无需踏进你的家门(只要它像他一样内置 ESP8266)。

在其他人的工作基础上，确定了通过 WiFi 连接控制机器的[简单命令](https://www.evilsocket.net/2016/10/09/IoCOFFEE-Reversing-the-Smarter-Coffee-IoT-machine-protocol-to-make-coffee-using-terminal/)(没有什么比 0x37 更能说明“给我沏杯好喝的咖啡”了)，【Martin】对 Smarter Coffee companion 应用程序进行了逆向工程，以提取和逆向工程其固件。他实际上能够找到打包在应用程序中的整个固件映像——这在空中下载(OTA)更新的世界中相对不常见，但在这种情况下很方便。使用[交互式反汇编程序(IDA)](https://www.hex-rays.com/products/ida/) 来筛选固件的内部工作，他确定了处理所有基本操作的功能，包括在屏幕上显示图像，控制加热元件，当然，还有哔哔声。从那里，他修改了股票固件映像，以包括一些恶意命令，并运行 OTA 更新。

这里令人难以置信的部分是，不仅固件是通过不安全的 WiFi 以未加密的明文形式传输的，而且机器甚至不需要用户按下按钮来确认更新。通过一次快速重启，陷阱就设置好了。机器正常运行，同时等待“66 号指令”，使其打开所有加热元件，启动内置研磨机，并发出嘟嘟声。不断地。

虽然一台坏掉的咖啡机看起来相对无害，但在硬件/固件安全方面有一些[相当重大的失误](https://hackaday.com/2014/08/05/hardware-security-and-a-dmca-takedown-notice/)，虽然可以避免，但一开始似乎就没有必要。这让我们想知道——为什么咖啡先生首先需要一部智能手机？

 [https://www.youtube.com/embed/bJrIh94RSiI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bJrIh94RSiI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【谢谢，阿基里斯和 STR-Alorman！]