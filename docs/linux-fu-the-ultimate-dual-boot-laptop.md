# Linux Fu:终极双开机笔记本电脑？

> 原文：<https://hackaday.com/2021/11/30/linux-fu-the-ultimate-dual-boot-laptop/>

我必须承认，除非绝对必要，我尽量不运行 Windows。但是因为很多原因，偶尔还是有必要的。特别是，我有几台对 Linux 很挑剔的笔记本电脑。我仍然经常双重启动它们，但是由于这样或那样的原因，我经常在它们上面留有窗口。我最近买了一台新的戴尔 Inspiron，它的双启动过程被证明是异常有效的，但也带来了一些挑战。

如果你想要一台合适的双启动笔记本电脑，你会对这种设置的工作原理感兴趣。当然，您总是可以对驱动器进行重新分区，但是笔记本电脑的驱动器相对较小，并且设置为专门用于 BIOS 诊断和恢复，因此在不破坏工厂工具的情况下重做驱动器总是一件痛苦的事情。

由于笔记本电脑配备了 512 GB 的 NVMe 驱动器，我想升级驱动器。因此，一种选择是安装一个更大的驱动器，然后走正常路线。这实际上是我的意图，但我最终走上了不同的道路。

## 坏消息，好消息

奇怪的是，这一切都解决了，因为我损坏了我买的第一台戴尔电脑的背光。我有延长保修期，每次“修理”后，它都以更糟糕的状态被退回。我上报了支持案例，他们提出只给我一台新电脑。问题是他们没有我的型号，所以他们给我提供了 Inspiron 5510 的升级版——比旧款更大的屏幕，更漂亮的键盘和更大的电池。但是还有一个重要的特征。

那个功能？双 NVMe 插槽。直到我打开箱子，我才意识到这台机器有双槽。有一个辅助短插槽(2230)和一个主插槽，可以容纳 2280(长)设备或 2230。在主插槽中，stock drive 是一个短单元。你会认为你可以只放入另一个短设备或翻转它们。你可以，但是没那么简单。

![](img/3d5ce49c8f2628c3b421618079c00ed8.png)

One M.2 slot is under the fan and there is another short slot to the right of the battery.

我想放入一个长外形的 2 TB 驱动器，所以我选择将短驱动器重新定位到短插槽。这很简单，机器启动时没有出现任何问题。我打开 BIOS，看看什么设置可以应用到两个驱动器上，发现了一些有趣的东西。默认的 BIOS 设置是针对 RAID 的。我想戴尔认为，如果您有一个驱动器，您并不在乎，如果您有两个驱动器，您可能希望它们显示为一个更大的驱动器。

当然，不同品牌的笔记本电脑可能不会这样设置，但这是值得检查的。我担心改变模式会导致硬盘无法使用。快速搜索显示，有些人已经改变了它，无法启动 Windows 了。然而，也有一个修复。

## RAID 不复存在(以及 Bitlocker 灾难)

诀窍是首先在 RAID 模式下引导到 Windows，然后使用 MSCONFIG 选择下次引导应该在安全模式下。然后重启，进入 BIOS，选择正常的磁盘配置。重新启动进入 Windows 安全模式。Windows 会注意到磁盘系统发生了变化，并在很少或没有注释的情况下放入正确的驱动程序。然后再次运行 MSCONFIG 关闭安全模式。然后，系统顺利启动。

另一件让我紧张的事情是，该驱动器打开了 Bitlocker 加密。我不确定戴尔是这样发货的，还是 Windows 11 决定加密驱动器。再说一次，除非你知道去哪里找，否则你不会真的被告知这件事，而且很难选择不去找。

如果您的驱动器被加密，请确保您知道如何获得您的密钥。最简单的方法是登录你的[微软账户](https://account.microsoft.com/devices/recoverykey?refd=support.microsoft.com)，理论上，所有连接到你账户的机器都应该有恢复密钥。不过，我会发现，情况并不总是这样，所以在纸上或 USB 驱动器上保存一份拷贝也是个好主意。

## 装置

[![](img/5a5bceca5dac1fa185d8cc56459b37a3.png)](https://hackaday.com/wp-content/uploads/2021/11/2021-11-09-13.55.40-www.dell_.com-d8d4ab74e09d.png)

Bracket instructions from the service manual.

下一项工作是安装新的 2 TB 驱动器。同样，您可能会有不同的问题，但在我的情况下，有一个小的螺纹支架安装主板，以接受驱动器螺丝，它是在一个短 NVMe 驱动器的位置。移除它需要一点努力，然后我不得不把它推回到另一个支架上，以适应一个长驱动器。[维修手册](https://www.dell.com/support/manuals/en-us/inspiron-15-5510-laptop/inspiron-5510--service-manual/removing-and-installing-components?guid=guid-7fbb11d7-9820-47bb-afaa-48fa912314d9&lang=en-us)解释了这一切。支架使用弹簧张力，所以需要一点力，但不要太大。

我在 YouTube 上找到了一个很好的升级这台电脑的指南。如果你在不同的笔记本电脑上工作，搜索类似的东西可能会有好处。

 [https://www.youtube.com/embed/zMVc8iDhzh4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zMVc8iDhzh4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



随着驱动器安装和背部松散连接，我很高兴看到 BIOS 识别驱动器没有问题。

## 让克隆人进来

有许多方法可以克隆 Windows 驱动器。我使用了 [Macrium Reflect](https://www.macrium.com/reflectfree?mo) ,它有一个自由层，这是你完成这个任务所需要的。老实说，在做这样的手术之前，你真的应该备份一些东西，但我承认我没有。实际上，我没有任何不能失去的东西。

Reflect 能够在克隆时自动扩展 Windows 分区，并在副本上取消加密。算是吧。拷贝进行得很好，但结果是 Windows 11 在注意到可能的时候会自动加密一个驱动器——至少在默认情况下。幸运的是，我发现了这一点，并打印出了新的加密密钥。然而，这并不像听起来那么聪明。

## 踢到头上

当然，现代的 UEFI 引导不像老式的那种那么简单，所以克隆后的重新引导仍然把我放在旧驱动器上，用 BIOS 强制引导确实有一次提示我输入解密密钥。我对自己感到满意，扔掉了解密密钥的打印件，但在此之前，我把它撕碎了。毕竟，现在 Windows 启动了，它会在我的帐户里，对吗？

[![](img/f44754678e815289ce5774b42f107238.png)](https://hackaday.com/wp-content/uploads/2021/11/error.png) 你可以猜到这是我的一个糟糕的假设。下面是我应该做的:我应该在 BIOS 中禁用旧驱动器，并在没有它的情况下测试重启。那是你应该做的。那不是我做的。结果，BIOS 仍然从旧驱动器上的 UEFI 分区引导，并重定向到新驱动器。因此，格式化旧驱动器会导致计算机无法启动，并出现常见的神秘非特定错误代码和无意义的日志文件条目。我可以从 USB 驱动器启动 Linux，但是所有的东西都加密了，不容易知道该怎么做。

启动一个 Windows 修复盘没问题，但是它需要在垃圾桶底部的解密密钥。我的微软账户仍然显示原始硬盘的旧密钥。幸运的是，尽管那天是垃圾日，垃圾车还没来，所以我就去翻垃圾箱找钥匙碎片。有了钥匙，启动修复还是不能修复一切。但至少我可以引导到一个命令提示符并运行常用的命令。最后，我有了一个可引导的系统。

## 没用的

不幸的是，微软账户问题依然存在。似乎没有办法强行把钥匙保存下来。互联网声称有一个选项可以保存帐户的密钥，但在 Windows 11 家庭版自动加密中，似乎不是这样。答案是从机器上删除 Microsoft 帐户，然后重新注册这些帐户。我怀疑如果我没有关联多个帐户，这可能不是一个问题，但是谁知道呢？

公平地说，只要您备份了您的密钥(我没有)，这就不是一个严重的问题。但奇怪的是，它只是悄悄地加密驱动器，然后未能为您存储密钥。

之后，将 Linux 安装到原来的驱动器上就没问题了。当然，GRUB 可以很容易地以你喜欢的任何配置启动机器，并且很容易改变。你必须做所有通常的双重启动的事情，比如将你的 Linux 时钟设置为本地时间，这样你就不会在每次重启时混淆时间。

## TLDR

如果你喜欢简短的总结:

*   有些笔记本电脑有两个驱动器插槽，因此您可以为 Linux 使用一个。如果你感兴趣的话，可以看看这个选项。
*   您的笔记本电脑可能默认配置了 RAID
*   引导 Windows 的克隆拷贝有一些挑战
*   Windows 11 可能会在不通知您的情况下加密您的驱动器，并且不会将恢复密钥保存到您的 Microsoft 帐户

不过，最终一切都解决了，现在我可以选择操作环境了。Linux 发现音频、网络和摄像头没有问题。这也有助于 5510 非常普通，没有像可拆卸屏幕和旋转传感器这样的东西，这些东西经常在其他笔记本电脑上混淆 Linux。

当然，你可以删除所有内容，安装 Linux 或者进行传统的双引导设置。或者[打造自己的笔记本电脑](https://hackaday.com/2021/07/28/it-takes-a-lot-to-build-a-hackers-laptop/)做自己想做的事情。你甚至可以用[覆盆子酱](https://hackaday.com/2017/02/12/raspberry-pi-laptop-uses-the-official-touchscreen/)来做这个。