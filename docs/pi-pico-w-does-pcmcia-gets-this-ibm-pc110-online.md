# Pi Pico W 做 PCMCIA，在线得到这个 IBM PC110

> 原文：<https://hackaday.com/2022/09/25/pi-pico-w-does-pcmcia-gets-this-ibm-pc110-online/>

将现代连接引入复古计算机是一个令人喜爱的领域——上世纪硬件和软件的简单性是一把双刃剑，通常，你会带来一台强大而小巧的现代计算机，以帮助其曾祖父与今天的网络对接。[yyzkevin]向我们展示了使用 Pi Pico W、 talking ~~PCI~~ ISA 构建的 PCMCIA WiFi 卡。这种卡为他的 IBM PC110 带来了现代的 WiFi 连接，而不需要为过时的标准设置单独的路由器，典型的 PCMCIA WiFi 卡受到这些标准的限制。

当然，RP2040 使用 PIO 引擎与 PCI ISA 对话。CPLD 帮助完成 ~~PCI~~ ISA 地址解码、一些多路复用以及 RP2040 的 3.3V 和 PCI 5 V 电平之间的电平转换。RP2040 软件模拟了一个 [NE2000](https://hackaday.com/2021/04/24/was-novells-ne2000-really-that-bad/) 网卡，这意味着过去的大多数操作系统都保证了驱动程序支持，并且软件集成似乎是无缝的。该卡已经可以让 PC110 上网，并且[yyzkevin]说他想对其进行改进——缩小设计，使其类似于典型的 PCMCIA WiFi 卡，将一些有用的功能绑定到 Pico 的 USB 端口，并且可能将他的 [PCMCIA SoundBlaster 项目](https://www.yyzkevin.com/pcmcia-soundblaster-clone-update/)集成到整个包中。

这是一个令人愉快的项目，它是如何实现其目标的，对于每个一直在观察 RP2040 的 PIO 引擎征服接口的人来说，这是一个惊喜，一般的微控制器通常无法实现。我们已经看到了[以太网](https://hackaday.com/2022/08/26/bit-banged-ethernet-on-the-raspberry-pi-pico/)、 [CAN](https://hackaday.com/2022/07/09/can-peripheral-for-rp2040-courtesy-of-pio/) 和 [DVI](https://hackaday.com/2021/02/12/bitbanged-dvi-on-a-raspberry-pi-rp2040-microcontroller/) 以及许多其他产品，毫无疑问，还会有更多产品问世。

 [https://www.youtube.com/embed/Pc2PUysWG2E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Pc2PUysWG2E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们感谢[Misel]和[Arti]与我们分享这些内容！