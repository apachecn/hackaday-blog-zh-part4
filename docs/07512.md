# 外来设备通过 Wireshark 和 Rust 获得 Linux 支持

> 原文：<https://hackaday.com/2020/08/20/exotic-device-gets-linux-support-via-wireshark-and-rust/>

如果你有一个开箱即用的好硬件，但不支持你的操作系统来获得它的全部功能，你该怎么办？[Harry Gill]发现自己在一个新的一体化(AIO)水冷系统中处于这种情况。从技术上来说，它不需要任何操作系统的交互来执行它的主要任务，但像设置调整或回读统计数据这样的事情只有 Windows 才有可能。他认为在 Linux 中也有这些功能会很好，因为通信是通过 USB 进行的，所以他认为显而易见的解决方案是[对协议进行逆向工程，然后简单地复制它](https://gill.net.in/posts/reverse-engineering-a-usb-device-with-rust/)。

他的第一步是建立一个双启动系统(他尝试在虚拟机中运行该软件，但不太成功)，这使他能够通过 Wireshark 和 USBPcap 捕获 USB 流量。然后，只需分析捕获的数据并编写一些 Linux 软件来理解这些数据。USB 任务的首选库是 libusb，它有很多语言的绑定，但是作为一个狂热的 Rust 用户，这个选择从来都不是问题。

然而，如何实际利用捕获的数据是一个完全不同的故事，在没有文档或来自供应商的帮助的情况下，[Harry]求助于良好的旧的试错法来找出哪个字节做什么。最终，他成功了，并且能够在 Linux 中获得他想要的额外支持功能——如果你想知道这在 Rust 中是什么样子，请查看 GitHub 库中的最终代码。

用 Wireshark 捕捉 USB 通信似乎是将不受支持的功能移植到 Linux 的一种很好的方式，正如我们之前看到的用 RGB 键盘和 VGA 帧抓取器启发的[。如果你想更深入地了解这个主题，[Harry]列出了一些关于 USB 的一般资源，但是](https://hackaday.com/2020/04/14/reverse-engineering-an-rgb-keyboard-under-linux/)[还有很多关于反向工程 USB](https://hackaday.com/2018/05/25/usb-reverse-engineering-a-universal-guide/)的资源可以探索。