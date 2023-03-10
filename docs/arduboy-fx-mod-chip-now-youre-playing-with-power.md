# Arduboy FX Mod-Chip:现在你在玩弄权力

> 原文：<https://hackaday.com/2021/03/04/arduboy-fx-mod-chip-now-youre-playing-with-power/>

传统上，一个充满技术用户的论坛试图将他们自己的硬件集成到游戏系统中，以获得对其整个软件库的自由访问权，这种事情会让索尼和任天堂的工程师夜不能寐。所谓的“mod 芯片”的发展和扩散对通过销售视频游戏赚钱的公司构成了生存威胁，因此，找出这些主机黑客并尽可能长时间地阻止他们的发现公开是当务之急。

但是 Arduboy 不是传统的游戏系统。它的游戏是免费分发的，所以一个允许用户一次将数百个游戏塞进掌上电脑的芯片并不是为了欺骗开发者，这是对现有硬件的一个实质性的可用性改进。因此，当 Arduboy 的创造者凯文·贝茨在官方论坛上发现草根阶层努力扩展系统的内部存储时，他没有试图阻止它。相反，他问如何帮助尽可能多的 Arduboy 所有者实现这一目标。

现在，在论坛成员 Blinky 先生发布他在系统测试板上悬挂外部 SPI 闪存芯片的最初概念不到三年后，[官方 Arduboy FX Mod-Chip 已经到来](https://arduboy.com/store/arduboy-fx-mod-chip/)。无论你是走 DIY 路线，构建自己的版本，还是购买现成的模块，有一点是肯定的:这是 Arduboy 的必备升级，将彻底改变你使用小型手持设备的方式。

## 选择的自由

最初我打算推出自己的升级，包括用一些细线将 W25Q128 等 SPI 闪存芯片焊接到 Arduboy 的 PCB 上，并使用 USBasp 等 ICSP 用新的引导加载程序刷新系统的 ATmega32U4 微控制器。虽然这不是一个用户友好的操作，但这个过程完全在普通黑客读者的能力范围之内，甚至可能是你可以用 bin 找到的部件做的事情。

[![](img/80367805dd9a82b716c17f5415cc3872.png)](https://hackaday.com/wp-content/uploads/2021/02/arduboymod_chip.jpg) 但是最后我决定直接用凯文的预编程 FX Mod-Chip。自从去年写了关于官方升级[的文章后，我一直很好奇，想看看顶级体验会是什么样的。凭借灵活的 PCB 和板载 ATtiny85，可以自动刷新系统的引导加载程序，这是一种更加简化的体验。加上只有 15 美元，它几乎没有打破银行。不过，如果你想省点钱，你可以花 9 美元买一个空白版本，然后在上面加载你自己的游戏。](https://hackaday.com/2020/08/04/official-arduboy-upgrade-module-nears-competition/)

无论哪种情况，最终结果都是一样的。现在你有足够的闪存来一次存储完整的 Arduboy 游戏库，而不是每次你想尝试一个新游戏的时候都必须将你的手持设备连接到 Arduino IDE。您可以使用非常流畅的视觉菜单快速轻松地按类型浏览它们，同时按住向上键和向下键，您甚至可以退出当前运行的游戏，选择其他游戏，而不必关闭系统。

 <https://hackaday.com/wp-content/uploads/2021/02/arduboymod_menus.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2021/02/arduboymod_menus.mp4](https://hackaday.com/wp-content/uploads/2021/02/arduboymod_menus.mp4)

就 Arduboy 而言，这次更新绝对是革命性的。坦率地说，该设备一次只能容纳一个游戏的事实总是让它比它应该有的使用起来更加麻烦。但是现在你可以快速跳过和尝试所有的游戏，而不用被束缚在电脑上，Arduboy 对于快速游戏会话来说更加实用。

## 装置

如前所述，官方升级包的设计考虑到了安装的方便性。如果你知道烙铁的尖端朝哪个方向，你应该没问题。对于任何需要更多指导的人来说，有一个书面的逐步安装指南，甚至还有一个视频可以观看。

[![](img/606483951c6be58acde46e0c4f8e6983.png)](https://hackaday.com/wp-content/uploads/2021/02/arduboymod_solder1.jpg)

Don’t blame me for that speaker wire.

[![](img/80554e412bc92c24728e80edf7706236.png)](https://hackaday.com/wp-content/uploads/2021/02/arduboymod_solder2.jpg)

取下后盖后，您只需将柔性 PCB 滑到电池下方，并钉住与板上测试焊盘对齐的八个点。您可以暂时移除压电扬声器，使安装变得更加容易，但这并不是绝对必要的。

一旦柔性 PCB 牢固连接，您需要重新打开 Arduboy，然后短接 GND 和 RST 焊盘大约五秒钟(一对镊子可以很好地完成这项工作)。这将触发 ATtiny85 开始引导加载程序刷新过程，很快您就会看到新的 Arduboy FX 启动屏幕。一旦确认更换了引导程序，您就可以重新启动系统。

## 图书馆管理

如果你购买了预编程的 FX Mod-Chip，你将立即获得 233 种不同的 Arduboy 游戏和应用程序，这些游戏和应用程序占用 W25Q128 芯片上 16 MB 可用空间中的大约 5 MB。虽然这并不代表为该平台编写的所有软件，但这是一个相当全面的集合。做出这种预测通常是一种让自己在未来看起来像个傻瓜的好方法，但在这种情况下，可以肯定地说 16 MB 对任何人来说都应该足够了。

但是添加未来的标题呢？毕竟，Arduboy 享受着活跃的开发者场景，并且总是有新的东西要检验。嗯，这就是事情变得有点棘手的地方。在撰写本文时，[官方工具实际上为芯片](https://github.com/MrBlinky/Arduboy-Python-Utilities)构建新的图像仍处于初级阶段。目前的方法依赖于一些 Python 脚本和手动管理的 CSV 文件，该文件将类别的嵌套目录链接到单个游戏二进制文件和横幅图像。这并不困难，但是听起来很不愉快。

不过也有一些很有前景的项目正在进行中，比如贾斯汀·戴维斯的 ArduManFX。这个多平台工具允许用户搜索、下载并最终安装 Arduboy 软件。截至目前，它只能将单个二进制文件闪存到系统中，但下一个版本将包括从其拖放 GUI 界面中创建芯片映像的能力。

[![](img/7a18ceeadf005e0af9bc4f71fd818a08.png)](https://hackaday.com/wp-content/uploads/2021/02/arduboymod_arduman.png)

For now, the flash builder interface is grayed out and can’t be selected.

## 这是方法

老实说，很难夸大这次升级对 Arduboy 体验的改善程度，并且毫不奇怪[扩展闪存存储将成为未来的标准功能](https://arduboy.com/store/arduboy-fx/)。对我个人来说，从数百款游戏中快速选择的能力赋予了这款设备新的生命，虽然我不愿意承认它已经开始变得有点脏了。现在它是一个小玩意，无论如何，一旦有地方可以去旅行，我一定会在旅行前把它扔进包里。

但也许更重要的是，Arduboy FX Mod-Chip 是一个光辉的例子，表明当一家公司不把客户当作敌人时会发生什么。凯文·贝茨不仅支持用户尝试修改他们购买的硬件，还深谋远虑地将他们的实验转化为正式产品，甚至将改进融入下一代 Arduboy。如果这种社区协作能够成为常态而不是例外，技术世界将会变得更加美好。