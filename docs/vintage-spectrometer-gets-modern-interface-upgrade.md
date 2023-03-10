# 老式光谱仪获得现代接口升级

> 原文：<https://hackaday.com/2021/04/01/vintage-spectrometer-gets-modern-interface-upgrade/>

有很多专业的、高端的科学设备在古董硬件和软件上运行。旧的实验室设备在 DOS 或其他古老的操作系统上运行并不罕见。当这些昂贵的工具被弃之不用时，它们往往会落入黑客手中，这些黑客在没有手册或支持的情况下，可能会试图让它们重新运行起来。macona 正试图用一台 740AD 光谱仪来做这件事，这台光谱仪是由 Optronic Laboratories 在 20 世纪 90 年代建造的。

最初，该设备配有一台完整的计算机-一台运行 DOS 和 Windows 3.0 的领先的 386SX25 PC。运行光谱仪的工具是用 BASIC 语言编写的。有了源代码，[macona]就能够在 LabVIEW 中重现该功能。为了取代原来的 ISA 接口板，使用了研华 USB-4751 数字 IO 模块，这与其内置的 LabVIEW 支持非常吻合。

随着事情的恢复和运行，[macona]已经对硬件进行了测试，测试了一些红外相机过滤器的性能。显然，这个硬件，或者说同一个模型，曾经被用来测试哈勃太空望远镜上使用的 CCD 的量子效率。

看到旧的实验室设备从垃圾箱中被拯救出来是很棒的，但是你不能总是依赖于你想要的东西被扔掉。在这种情况下，你必须从头开始建立自己的公司。休息后的视频。

 [https://www.youtube.com/embed/AlwsedCNjxk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AlwsedCNjxk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

