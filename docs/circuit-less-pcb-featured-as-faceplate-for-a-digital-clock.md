# 用作数字时钟面板的无电路印刷电路板

> 原文：<https://hackaday.com/2022/08/17/circuit-less-pcb-featured-as-faceplate-for-a-digital-clock/>

如果印刷电路板上没有电路，它会不会不再是一个“PCB ”,而可能只是一个“PB ”?

不管你怎么称呼它们，PCB 已经变得如此便宜，而且易于设计和制造，这一事实使它们有了更多创造性的用途，而不仅仅是作为一个项目的布线。在这种情况下，[杰里米·库克]将其中一个作为他的[“742 时钟”](https://github.com/JeremySCook/clock742)的面板，这个名字是基于他的七段显示器有 42 毫米高，而且它是“24/7”向后的事实。

除了容纳 Wemos ESP32 模块和 led 的实际电路板之外，还设计了一个无电路板，在阻焊膜中留有间隙，用作光导管。夹在两块板之间的是一个 3D 打印的面具，用来控制光线，并引导光线只通过光导管。[Jeremy]经历了几次扩散器和面罩设计的迭代，最终得出了一个既好用又好看的组合。他提到了一种可能的面板重新设计，包括一个铜背板，以提高不透明度，我们认为这是一个好主意。我们还想看看不同的底物是如何工作的；不同厚度的板或使用不同玻璃化转变温度的 FR-4 会更好吗？看看下面的视频，看看你有什么想法。

我们看到越来越多的 PCB 作为结构元件出现，从[外壳](https://hackaday.com/2019/09/16/the-benefits-and-pitfalls-of-using-pcbs-as-an-enclosure/)到[控制面板](https://hackaday.com/2021/01/30/master-video-call-control-panel-is-made-of-pcbs/)和[甚至工具](https://hackaday.com/2022/01/18/ultra-cheap-pcb-wrenches-make-perfect-kit-accessory/)，我们赞同这一趋势。但我们真正认可的是[杰里米]在这里所做的，他让这个时钟只是一个愚蠢的显示器，通过 NTP 获得网络时间。要是我们厨房里的三个数字钟都做同样的事情就好了——也许这样它们就不会一分钟都和另一分钟不同步了。

 [https://www.youtube.com/embed/BssHpYaKQ-s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BssHpYaKQ-s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

