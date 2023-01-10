# 对树莓 Pi GPIO 的狂热滥用

> 原文：<https://hackaday.com/2021/04/06/fan-tastic-misuse-of-raspberry-pi-gpio/>

[River]是家庭自动化的忠实粉丝。搬进新房子后，[他想将两个无线控制的风扇灯融入他的家庭自动化系统](https://riveducha.onfabrica.com/decode-wireless-signal-with-usb-tv-tuner)。问题是这样的:虽然风扇是无线的，但它们的频率和协议与家庭自动化系统不兼容。

第一步是确定风扇遥控器使用的频率。虽然公开的 FCC 记录会揭示操作的频率，但[River]认为使用便宜的 USB RTL-SDR 和 Spektrum 程序来扫描可能的频率范围会更快，并很快发现风扇说话 304.2 MHz。

接下来是逆向工程协议。[通用无线电黑客](https://hackaday.com/2017/02/23/universal-radio-hacker/)是一款工具，旨在使用 RTL-SDR 相对轻松地破译未知的无线协议。[River]用它数字化了一个按键，并立即识别出这是一个简单的开关键控(OOK)。有了这些知识，他将所有七个按钮的无线电命令数字化，并很快就能够逆向工程整个协议。

[River]想要使用树莓 Pi 将风扇引入他的家庭自动化系统，但是树莓 Pi 没有 304.2 MHz 无线电。它拥有用户可编程 GPIO 和 rpitx 封装，可将 GPIO 引脚转换为基本的无线电发射器。当然，Pi 的 GPIO 引脚不够长，无法在 304.2 MHz 下有效传输，所以[River]添加了一个合适的天线，以及一个低通滤波器来清理传输的信号。rpitx 包支持开箱即用，所以[River]很快就能让 Pi 控制他的风扇！

如果你想做一些更低成本的家庭自动化，看看这种方法[使用树莓 Pi 来控制一些廉价的智能插头](https://hackaday.com/2019/01/19/automate-your-home-from-the-clearance-rack/)。