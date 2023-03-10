# GPU RAM 升级比你想象的更近

> 原文：<https://hackaday.com/2022/01/30/gpu-ram-upgrades-are-closer-than-you-think/>

我们都习惯于在台式机和笔记本电脑中交换内存。那么 GPU 呢？[dosdude1]告诉我们，焊接 RAM[仅仅是一个有待征服的领域](https://www.youtube.com/watch?v=QRrThOEmjOU)。当然，进行这样的努力肯定有一个很好的理由——在他的情况下，他找不到可以用苹果 BIOS 刷新的特定类型的 Nvidia GT640，以使他的 Xserve 机器正确输出苹果启动屏幕。他能找到的只有 1GB 的版本，而苹果的 BIOS 只能闪存到 2GB 的版本上。在速卖通上获得 2GB 的 DDR 芯片实在太诱人了！

该视频讲述了整个更换过程，直到你可以自己重复一遍——只要你有预热器，这是返工相对较大的 PCB 所必需的，以及一套更换 BGA 芯片的常规工具。最后，卡启动了，并闪了一个新的 BIOS，成功地显示了苹果启动标志，如果没有特殊的苹果 VBIOS 酱，通常会丢失。如果你曾经想尝试这样的维修，现在你少了一个借口-而且，GT640 是一个相对旧的卡，你甚至不会冒那么大的风险！

这不是我们最近报道的第一次焊接 RAM 更换之旅-这里是我们关于 [[Greg Davill]在他的戴尔 XPS](https://hackaday.com/2021/11/24/you-cant-upgrade-soldered-on-laptop-ram-think-again/) 上升级焊接 RAM 的文章！你也可以这样升级 CPU。虽然这是足够先进的笔记本电脑维修店的标准程序，但即使是业余爱好者也可以通过适当的设备和足够的运气来管理它，正如[EEE PC CPU 升级所展示的](https://hackaday.com/2012/08/10/swapping-out-eee-pc-bga-chip-for-1-6-ghz-upgrade/)。BGA 工作和苹果电脑获得第二次生命是携手并进的——就在两年前，我们报道了这个 [BGA 钻孔黑客绕过 Macbook](https://hackaday.com/2020/06/28/a-dead-macbook-gpu-shouldnt-stop-you-with-this-bga-soldering-hack/) 中一个失效的 GPU，在此之前还有一个 [Macbook 水渍复活的故事](https://hackaday.com/2019/07/09/liquid-damaged-macbook-saved-with-a-keen-eye/)。

 [https://www.youtube.com/embed/QRrThOEmjOU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QRrThOEmjOU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

