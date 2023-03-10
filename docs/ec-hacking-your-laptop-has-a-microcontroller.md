# EC 黑客:你的笔记本电脑有一个微控制器

> 原文：<https://hackaday.com/2022/06/07/ec-hacking-your-laptop-has-a-microcontroller/>

最近，我偶然发现了[一篇由【DHowett】，](https://www.howett.net/posts/2022-04-adding-an-ec-feature-1/)撰写的关于重新编程一台框架笔记本电脑的嵌入式控制器(EC)的很酷的文章。他向我们展示了如何重复使用 Caps Lock LED，而不是让它指示 F1-F12 键层状态，也称为“Fn lock”，也就是“你的 F1 键目前是作为 F1 工作，还是调节音量”。他指导我们向笔记本电脑的 EC 固件添加定制代码，并将其正确集成到 EC 运行的各种例程中。

该框架使用的 EC 是 Microchip 的 MEC1521 芯片，今年早些时候，他们为它开源了固件。现在，有一个微控制器代码的[库，你可以自己编译，并用它来刷新你的框架笔记本电脑的主板。在 HackerNews 的评论部分，一位框架代表推测，你可以通过 EC 固件黑客](https://github.com/FrameworkComputer/EmbeddedController)[将 GPIOs 添加到框架主板](https://news.ycombinator.com/item?id=31092013)。

等等……微控制器代码？GPIOs？这就给我们带来了一个问题——EC 到底是什么？首先，它只是一个微控制器。您可以在每台 x86 计算机中找到一个 EC，包括笔记本电脑，管理您计算机的低级功能，如电源管理、键盘、触摸板、电池和许多其他东西。在 Apple land，你可能知道它们是 SMC，但它们的功能是一样的。

为什么我们一直没有重新编程我们的 ECs？这也是一个值得考虑的问题，我会告诉你一切。

## 选委会的工作是什么？

EC 控制着你笔记本电脑里的一大堆设备。不包括连接到 USB、LVDS/eDP 或 PCIe 的设备，因为这些属于芯片组的范围。相反，这些是像电源开关、充电器芯片和各种电流监控器这样的设备，因为即使在芯片组和 CPU 断电的情况下，这些设备也必须正确工作。当然，这不仅仅是电源管理，笔记本电脑中有很多东西都需要 GPIOs 来实现。

[![section from the EEE PC 701 schematic, showing the EC connections, and even some unused functions like extra button connections](img/da860e2bf6c576e8f48a15f00f411c1c.png)](https://hackaday.com/wp-content/uploads/2022/05/hadoc_embedded_controller_pic1.png)

The EC of a EEE PC 701\. This one even has some extra signals for media buttons that were left out in hardware!

一般来说，你用`digitalWrite`控制或用`digitalRead`监控的任何东西，通过 ADC 测量，或用 I2C 说话——这些都是 EC 处理的事情。因此，EC 读取电池状态和充电器电压，用 PWM 驱动风扇，并从各种传感器获取温度测量值。笔记本电脑键盘是一个按键矩阵，EC 扫描该矩阵并处理按键，将按键事件转发到芯片组，然后由操作系统读取。无论您的触摸板是 PS/2 还是 I2C，EC 都会处理它，并将其暴露给操作系统。

您笔记本电脑的电源按钮直接连接到 EC。结果，你的 EC 是第一个通电的东西；如果你的坏掉的笔记本电脑对电源按钮没有反应，这意味着无论出于什么原因，EC 都无法完成其电源管理工作。事实上，如果你查看 Framework laptop 最近发布的[简化示意图，](https://github.com/FrameworkComputer/Mainboard/blob/main/Electrical/Mainboard_Interfaces_Schematic.pdf)你会看到 EC 有自己独立的电源轨，直接来自电池。

它是如何与芯片组对话的？大约二十年来，ECs 一直使用 LPC 总线——一种表面上类似 qSPI 的四位宽总线。除了 ECs，它只是在最近才真正被 TPMs 使用。LPC 使用 25MHz 到 100MHz 的频率。因此，如果你想对你的 LPC 信号进行逻辑分析并捕获一些数据包，你典型的 cheapo 25Msps LA 不会这样做，但一个现成的 FPGA 板或一种更快的 LA 将创造奇迹，并且有一个[非常酷的文件](https://dl.acm.org/doi/10.1007/978-3-642-29804-2_12)使用 LPC 操作和 FPGA 从 TPMs 中提取密钥。

LPC 大约有 20 年的历史，是 is a 总线的直接继承者——事实上，在 2003 年的一些笔记本电脑原理图中，你会发现 EC 通过 ISA 连接，但除此之外都是 LPC。然而，最近的 EC 转而使用 eSPI，[一个类似 qSPI 的接口来代替 LPC，](https://www.totalphase.com/blog/2021/09/what-is-the-espi-protocol-and-how-does-it-improve-upon-lpc/)框架 EC 也使用 eSPI。

## 当然，这涉及到固件

每个 EC 都有固件，每台笔记本电脑(以及台式机和服务器！)有一个 EC。EC 固件几乎总是闭源的。因此，当我们谈论计算机内部的专有部件时，EC 固件是我们容易忽略的二进制程序之一。通常，EC 固件与 BIOS 存储在同一个 SPI 闪存芯片上，其他时候，有一个单独的外部或片内闪存，在这种情况下，您通常有一个 UART 引导加载程序，可以通过它刷新 EC。所有这一切都取决于具体的制造商和型号的 EC 你有。

通常，您的 EC 是建立在 ARM 或 8051 架构上的，其他时候它是更模糊的东西，如 CompactRISC。最常见的是，当涉及到你的 EC 固件时，你最多只能得到一个二进制的 blob。在某个时候，当谷歌进入笔记本电脑业务时，他们的一群工程师可能会说“够了”，然后[开源了他们的 EC 代码](https://chromium.googlesource.com/chromiumos/platform/ec/)——这是框架在涉及到他们自己的 EC 固件时一直在构建的。去年， [System76 开放了他们的 EC 代码，](https://puri.sm/posts/librem-14-adding-librem-ec-freed-embedded-controller-firmware/)也是。不幸的是，对于其他笔记本电脑制造商来说，形势依然严峻。

你的 EC 会被后门吗？不太可能——修改和更新 EC 固件往往比修改和更新 BIOS 映像更难。现在，你能自己改变你的 EC 的行为吗？这至少在技术上是可能的，我认为你应该一直能够做到这一点。

## 那么，黑客呢？

当然，对于笔记本电脑的每个子系统，你会发现 Thinkpad 爱好者的一个小组已经深入研究并使用它来完成一些有趣和有用的事情。EC 就是这样一个方面，他们[肯定有一些东西可以提供](https://github.com/hamishcoleman/thinkpad-ec)——主要是重新编程键盘布局和移除电池锁。通过键盘布局，他们已经成功地让旧的(显然更高级的)键盘与新的笔记本电脑一起工作，[一个教程](https://www.thinkwiki.org/wiki/Install_Classic_Keyboard_on_xx30_Series_ThinkPads)谈论你需要如何具体绝缘某些引脚，以及[一个超级方便的方法来快速改变。](https://www.reddit.com/r/thinkpad/wiki/ecmod)

然而，电池部分更为重要——你往往可以忍受一个不合格的键盘，即使是在本应是一流的 ThinkPads 上。问题是 EC 中的“正版”电池检查，如果电池没有通过，它不会让你充电(甚至操作)。这不仅仅是限制了第三方电池的选择，如果听起来是这样的话——这种检查也禁止使用联想电池，这些电池只是为了不同类型的 Thinkpad，但在其他方面机械，电气和电子方面完全合适。

 [https://www.youtube.com/embed/Fzmm87oVQ6c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fzmm87oVQ6c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



有一个关于 ThinkPad EC 黑客攻击如何展开的视频，我建议你去看看。现在，联想似乎不喜欢人们交换键盘和使用第三方电池，联想自己也不再出售“正版”电池了。因此，在某个时候，他们决定[关闭 EC 固件更新最舒适的方式之一](https://support.lenovo.com/gb/en/solutions/len-27764)，并以“安全改进”为由发布 BIOS 更新。相关的 CVE 是这样说的:

> 旧 ThinkPad 系统的各种 BIOS 版本中报告了一个漏洞，该漏洞可能允许具有管理权限或物理访问权限的用户使用未签名的固件更新嵌入式控制器。

如果你问我，这种描述是疯狂的。这句话本质上的意思是“笔记本电脑的所有者可以闪存未经联想批准的 EC 固件”。我确实想知道是什么导致了它，以及可能的理由是什么，但最终，不管是什么原因，它都分散了我的信仰。也就是说，在自己的笔记本电脑上更新 EC 固件应该是可能的，联想关闭了一个用户友好的方式来做到这一点。

此外，毫无疑问，并不是所有的制造商都尊重你的权利，维修时，涉及到 ECs。例如，近十年来，戴尔一直为其笔记本电脑提供 EC，这些 EC 具有加密的固件和融合在 EC 中的密钥。这对于戴尔笔记本电脑维修来说是一个特别的问题，因为 EC 经常会死亡。虽然您可以购买一个空白的 EC 并将其回流以取代戴尔的死 EC，但它不会有戴尔在工厂闪存到 EC 中的解密密钥，因此不会运行戴尔的加密固件。修改在这里是不可能的——当你的笔记本坏了的时候，甚至不可能找到合适的替代品来代替 EC，即使芯片本身是丰富的。

## 你现在能做什么？

现在有三家制造商拥有 ECs 的开源固件——Google、System76 和 Framework。但是，你能用这个固件做什么呢？正如任何未被充分利用的黑客领域一样，实现其全部潜力需要时间。重新映射按键并不是唯一的事情——如果笔记本电脑的制造商没有为您提供电池寿命，您可以实施 80%的电池充电限制，在不需要任何操作系统支持的情况下为您的笔记本电脑键盘添加额外的层，也许可以调整您的风扇曲线。或者，事实上，你可以在笔记本电脑中添加一些 GPIOs，用于你想要的任何传感器或按钮。

您还可以修复错误，这些错误时不时会在 EC 中出现，处理起来可能会很烦人——想象一下[键盘按键时不时会卡住](https://community.frame.work/t/function-fn-keys-sticking-fix-for-linux/10156),看似随机，这正是当您有 EC 错误时会发生的情况。Bug 修复或改进，就像目前对我们关闭的任何固件一样，我们不会从明天开始看到大量很酷的黑客，但当谈到 EC 黑客时，肯定会有很酷的东西出现。