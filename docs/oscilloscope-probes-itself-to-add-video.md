# 示波器自行探测以添加视频

> 原文：<https://hackaday.com/2021/11/24/oscilloscope-probes-itself-to-add-video/>

现代示波器通常加载了各种功能，但有时你会遇到一个看似容易实现却不可用的功能。[kgsws]想要使用他的 Rigol DS1074 在他的 YouTube 视频中显示现场测量，但发现这个示波器不支持视频输出。不被吓住，[kgsws]决定[自己加这个功能](https://www.youtube.com/watch?v=sM5IHYPGXds)。在下面嵌入的视频中，他详细描述了为示波器添加 USB 视频采集(UVC)接口的过程。

基本想法是找到进入示波器显示器的信号，并使用 Cypress EZ-USB 板读出它们。这是一个开发板，可以用来设计 USB 设备，并支持 UVC 模式。然而，由于没有 Rigol 内部电路的任何文档，因此[kgsws]必须探测显示器连接器，以找出哪个引脚承载哪个信号。因为除了这个 Rigol 以外，他没有其他可用的观测仪器，所以他把拆卸下来的仪器的各个部分连接起来，这样它就可以(笨拙地)探测自己的内部信号。

在映射出自己的显示信号后，是时候将它们连接到 EZ-USB 板上了。[kgsws]通过将大约 24 根细线焊接到主板上的 SMD 焊盘上实现了这一点。EZ-USB 板本身被放在示波器外壳的后面，但为了节省空间和电力，不得不去掉不需要的组件。一个非常聪明的技巧是添加了一个簧片开关，它允许[kgsws]将 EZ-USB 板设置为编程模式，而不必打开示波器的外壳，只需在开关附近放置一块磁铁。

将一个 USB 连接器焊接到 RF 屏蔽罩的备用插槽中后，项目就完成了。Rigol 现在可以连接到 PC，只是作为一个视频捕获设备出现，随时可以为[kgsws]未来的项目视频进行流式传输或捕获。我们已经看到 Rigol DS1000Z 系列上的其他黑客攻击，以[捕捉一系列截图](https://hackaday.com/2021/05/26/yet-another-rigol-ds1054z-viewer/)或[启用额外的带宽和功能](https://hackaday.com/2014/11/12/how-to-get-50-more-zed-from-your-rigol-ds1054z/)，但添加直播视频输出目前还不是选项之一。

 [https://www.youtube.com/embed/sM5IHYPGXds?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sM5IHYPGXds?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

