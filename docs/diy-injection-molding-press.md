# DIY 注射成型机

> 原文：<https://hackaday.com/2021/01/01/diy-injection-molding-press/>

虽然 3D 打印现在已经变得容易获得和便宜，但仍然有几个用例需要注射成型提供的优势，即使是小批量运行。专业的小批量注射成型可能会非常昂贵，购买手动机器可能会花费相当多。当然，有许多 DIY 注射成型项目可供选择，但它们通常涉及相当数量的工具和劳动力。[Bolzbrain]想要绕过所有繁重的切割、焊接和框架组装工作，所以他用一台现成的[六吨液压机](https://www.wiltec.de/industrial-hydraulic-workshop-bench-press-6t-pressure-shop-garage.html)为自己建造了一台 [DIY 注塑压机](https://hackaday.io/project/176393)。最后，他花了大约 150€买了这台机器，又花了 120€买了组装机器的工具。他还设法找到了一家便宜的本地数控服务公司，这让他在加工模具方面赚了不少钱。当然，你不能用金钱来衡量学到的东西和手工制作的满足感。

选择液压机是一个好主意，因为它提供了工作所需的高压，而操作者不必付出很大的努力，这是其他一些 DIY 机器的一个大缺点。另外，结构框架非常坚固，非常适合这种用途。这种机器的另一个主要部分是加热注射块，有几种不同的方法。在研究了一些可能的解决方案后，他决定建造一个加热的铝块，通过它可以使用液压活塞冲压塑料颗粒。加热由一对 500 瓦加热器提供，k 型热电偶进行温度传感。工业 PID 控制器通过固态继电器调节块温度。总的来说，电气和机械布局不能再简单了。

[Bolzbrain]在记录他的一系列视频方面做得很好，越来越多看着这些视频的干瘪的黑客会在座位上蠕动，发现无数的失败。他买了他能买到的最便宜的基座钻孔机，看着钻孔机在铝块上打出一个 26 毫米的孔，感觉很不舒服。

[![](img/f42c700a69f9f251a0fc7b86ab40a982.png)](https://hackaday.com/wp-content/uploads/2020/12/DIY-injection-molding-twin-500W-heaters.jpg) 电气布线有很大的改进空间 220V 交流加热器、裸露的布线和用一对夹子夹住的应急面板。安装和移除模具是一项任务，需要大量摆弄几个 C 形夹钳，这需要在每次拍摄时重复进行。也许肘节夹可以帮助他简化模具的安装和拆卸。一旦他弄清楚了[关于脱模剂和壁面拔模斜度](https://hackaday.com/2020/04/19/gain-an-understanding-of-injection-moldings-design-gotchas/)，他就不必费力地试图将模制品从模具中取出。然后是正确的流道设计问题，以便热塑性塑料可以快速完全填充模具型腔，没有任何口袋。

但最终，最重要的是他得到了符合他目的的相当好的模制零件。随着更多的调整和渐进的改进，我们相信他会得到更好的结果。休息后的视频是对他的构建的简短概述，但项目页面有一系列详细的视频，涵盖了项目的各个方面。如果您想了解桌面注塑成型，请查看“[面向家庭游戏玩家的台式注塑成型](https://hackaday.com/2020/10/16/benchtop-injection-molding-for-the-home-gamer/)

 [https://www.youtube.com/embed/-9W2gR-gwfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-9W2gR-gwfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

