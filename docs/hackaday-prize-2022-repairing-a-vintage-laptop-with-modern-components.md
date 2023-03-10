# 2022 年黑客日奖:用现代部件修复老式笔记本电脑

> 原文：<https://hackaday.com/2022/07/27/hackaday-prize-2022-repairing-a-vintage-laptop-with-modern-components/>

今天，笔记本电脑可能无处不在，但曾几何时，它们是富有商人的专属领地。早在 90 年代初，很少有人愿意支付可移植性的额外成本。结果，那些日子的笔记本电脑没有多少幸存下来；对于那些这样做的，保持它们运行可能是一个相当大的挑战，因为它们的紧凑结构和非标准组件的使用。

[Adalbert]在得到一台 1991 年的东芝 T3200SXC 时遇到了这些问题。作为有史以来第一台配备彩色 TFT 显示屏的笔记本电脑，它非常值得作为历史文物保存下来。可悲的是，原来的显示器不再工作:它只显示了一个非常微弱的图像，并在不久后完全空白。漏电的电容器破坏了电源板，使笔记本电脑完全没电了。[Adalbert]然后开始考虑他的选择，从试图修复原始组件到把所有东西都拆下来，并把它变成一个现代电脑在旧箱子里的项目。

最后，他选择了两者之间的一个选项，我们作为保护主义者只能鼓掌:他用一个尺寸和分辨率合适的现代显示器取代了显示器，并建立了一个新的定制电源，尽可能保持计算机的其余部分完好无损。[Adalbert]在下面嵌入的视频中描述了整个过程，并在他的 hackaday.io 页面上介绍了许多细节。

连接现代 LCD 屏幕并不像看起来那么困难:旧显示器有一个 RGB TTL 接口，每种颜色三位，新显示器有一个非常相似的系统，每种颜色六位。[Adalbert]制作了一个适配器 PCB，只需将笔记本电脑的三位连接到屏幕上最高的三位。一组 3D 打印的支架确保了新屏幕在经典情况下的安全贴合。

[![The internal power supply module of a laptop](img/43f60eedbfa1c680716ee140cce6bb7b.png)](https://hackaday.com/wp-content/uploads/2022/07/Toshiba-T3200SXC-PSU.jpg) 对于电源【Adalbert】采取了类似的做法。他设计了一个带有几个 DC/DC 转换器的 PCB，可以很容易地放入电脑机箱，留下足够的空间来添加电池。这使得旧东芝比以往任何时候都更便携——信不信由你，最初的 T3200SXC 只能通过电源连接使用。

一旦笔记本电脑恢复工作状态，[阿达尔伯特]增加了一些收尾工作:声卡和扬声器使它适合作为游戏平台，网卡使它具备了基本的在线功能。最终的结果是 T3200SXC 的外观和感觉与新品完全一样，但增加了一些功能。这是一个真正令人满意的结果:许多经典的笔记本电脑项目[添加了现代计算硬件](https://hackaday.com/2021/06/30/installing-linux-like-its-1989/)，甚至[完全取代了原来的内容](https://hackaday.com/2022/04/02/compaq-286-laptop-gets-raspberry-transfusion/)。你可能还想了解一下【阿达尔伯特】的[不寻常的基于 3D 打印机的 PCB 制造技术](https://hackaday.com/2022/07/26/a-new-way-to-produce-pcbs-with-your-3d-printer/)，他将这种技术用于新的电源。

 [https://www.youtube.com/embed/kXoOnAgggJo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kXoOnAgggJo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)