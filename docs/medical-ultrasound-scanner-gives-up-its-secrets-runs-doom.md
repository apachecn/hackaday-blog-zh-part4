# 医用超声波扫描仪泄露秘密，走向灭亡

> 原文：<https://hackaday.com/2022/12/18/medical-ultrasound-scanner-gives-up-its-secrets-runs-doom/>

医疗设备往往会成为有趣的拆卸视频:认证机构强加的严格要求意味着你会发现高质量的组件和高标准的设计和制造。但是当[购买它修复它]在易贝买了一台超声波扫描仪时，他并没有兴趣拆掉它:他的计划是用它来发现他的羊是否在羔羊体内，所以他继续修复它，并为它的新用途进行修改。

有问题的设备是 Mediwatch Bardscan II，用于扫描人的膀胱。然而，主板具有完全不同的型号，这表明基本设计用于几种类型的超声波扫描仪。该系统由 AMD Geode 处理器提供支持，该处理器运行存储在 CompactFlash 卡上的 Windows XP Embedded，因此检查内部软件很容易:扫描仪界面甚至可以在普通的 Windows PC 上运行。

[![](img/9bd6e465d79a388fb4156305eef6bddf.png)](https://hackaday.com/wp-content/uploads/2022/12/ultrasound_detail.jpg) 内部驱动器上的几个文件指向隐藏的特征，文件名如`kidney.dib`和`liver.dib`表示仪器可以扫描的不仅仅是膀胱。该驱动器还包含几个版本的扫描应用程序，以及一个可以启用或禁用许多功能的`.ini`文件。通过 x32dbg 运行可执行文件，[Buy It Fix It]甚至能够恢复密码来启用“高级设置”菜单——如果你想知道的话，它是“u10”。

通过一点文件编辑，[Buy It Fix It]成功地将这个相当基础的系统变成了一个更加灵活的超声波扫描仪。例如，他现在可以调整扫描深度，重放以前的扫描，并在任何捕获的图像上做笔记。正如他在视频最后演示的那样，它甚至可以运行*DOOM*——尽管我们可以想象他的羊可能不喜欢看到它们的主人拿着一个装满火焰投掷恶魔的盒子走近它们。

已经出现了很长时间的医疗超声波扫描仪可能看起来是复杂的机器，但有可能用容易获得的组件将 T2 变成简单的版本。

 [https://www.youtube.com/embed/pdQRYp7sCPQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pdQRYp7sCPQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

