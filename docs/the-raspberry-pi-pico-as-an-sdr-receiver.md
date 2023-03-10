# 作为 SDR 接收器的 Raspberry Pi Pico

> 原文：<https://hackaday.com/2021/03/16/the-raspberry-pi-pico-as-an-sdr-receiver/>

随着廉价 RTL-SDR 设备的大量出现，以及功能更强的 SDR 价格的不断降低，我们十年或更久以前满意的低带宽设备似乎没有多少空间了，但从如此简单的东西中仍然可以学到很多东西。Luigi Cruz 向我们展示了一个简单的 SDR，它使用了 Raspberry Pi Pico 的模数转换功能，由于它可以与 GNU Radio 一起工作，我们认为这是一个非常好的项目。 [CNX 软件公司拥有完整的故事](https://www.cnx-software.com/2021/03/11/picosdr-a-raspberry-pi-pico-powered-sdr-based-on-gnu-radio/)，并很快透露，凭借其每秒 50 万个样本的带宽，即使将奈奎斯特定律推到极限，它也不是一台会让 SDR 世界着火的机器。

因此，除了时间信号和一些长波广播电台(如果你住在仍然有它们的地方),你将需要一个滤波器和接收转换器来利用这个 SDR 引入任何无线电方面的有用信息。但是，一个基带 SDR 具有数百 kHz 的有用带宽和通过 GNU Radio 轻松入侵的能力，只需一个树莓 Pi Pico 的微不足道的成本，就值得再看一眼。你可以在休息时间下面的视频中看到它的作用，如果你不知道该怎么办，可以看看[迈克尔·奥斯曼和凯特·特姆金的 2019 年超级会议演讲](https://hackaday.com/2020/02/21/software-defined-everything-with-mike-ossmann-and-kate-temkin/)。

 [https://www.youtube.com/embed/okIkjC02J_M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/okIkjC02J_M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

