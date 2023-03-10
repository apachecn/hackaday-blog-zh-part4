# 特斯拉召回 EMMC 故障汽车，称零件 A 为“易损件”

> 原文：<https://hackaday.com/2021/02/11/tesla-recalls-cars-with-emmc-failures-calls-part-a-wear-item/>

这是任何花了大量时间玩树莓派的人都熟悉的问题——随着时间的推移，SD 卡中的闪存达到其写入周期限制，并在完全失败之前导致一连串令人困惑的错误。虽然闪存存储速度快、体积小、机械性能可靠，但它的可写寿命总是比磁性技术短得多。

![](img/32ba8219dc8e959425a5216944b62c1b.png)

Flash storage failures in the computer behind Tesla’s famous touch screen are causing headaches for drivers.

当然，通过适当的磨损均衡技术和谨慎使用，这些问题可以成功缓解。令人惊讶的是，当一家大型汽车制造商未能实现这些基本功能时，就像特斯拉的几款车型一样。由于该车的 Linux 操作系统过度登录其 8 GB eMMC 存储，闪存模块已经磨损。这导致汽车普遍出现故障，通常会使汽车进入跛行模式，并禁用许多通过触摸屏控制的功能。

由于该问题影响到重要的子系统，如加热器、除霜器和警告系统，NHTSA 在 1 月份写信给汽车制造商，要求召回。[特斯拉的回应有些惊愕地默认了这一请求](https://www.bbc.com/news/technology-55902779?at_custom1=%5Bpost+type%5D&at_custom2=twitter&at_campaign=64&at_medium=custom7&at_custom4=682A08D6-6550-11EB-867C-E2F04744363C)，淡化了问题的严重性。现在，他们声称，焊接到主板上的球栅 eMMC 芯片，不拆卸仪表板就无法接触到，并且在用户手册中没有明确提到，应该被视为“磨损项目”，因此不应该受到这样的审查。

## 肯定是一件奇怪的衣服

![](img/cb30e03c2e6fb5a87c87a92c6410aae9.png)

The chip in question, a sub-$7 eMMC chip packing 8GB of storage.

历史上，汽车中的主要电子部件不被视为消耗品。虽然一些汽车面临发动机控制单元或车身控制模块的问题并不罕见，但它们通常不被视为定期更换的磨损件。迄今为止，先例认为这些零件可以维持车辆的使用寿命，并在意外故障的情况下更换。特斯拉案例的不同之处在于，eMMC 的失败大体上是不可避免的。不像偶尔的制造缺陷所预期的那样，这是一小部分汽车中的孤立故障，而是一个影响到某个特定日期下线的每辆汽车的问题。在某些生产月份，故障率高达 30%。由于电脑和触摸屏控制着如此多的重要车辆功能，它不是一个容易被最终用户忽视的缺陷。

![](img/2d87ef51f010604895de4fc7198629fa.png)

Replacing the chip involves reflowing the board, [and carefully pulling off the offending part with tweezers](https://www.youtube.com/watch?v=-wCaBDUQySI&feature=emb_title).

[Tesla 断言 eMMC 芯片应被视为“磨损物品”](https://static.nhtsa.gov/odi/inv/2020/INRL-EA20003-82493P.pdf)充其量是一个可疑的说法。闪存确实会磨损，这是事实，正如特斯拉在讨论该技术的局限性时指出的那样。随着时间的推移，现代汽车上的许多部件都会磨损——刹车片、皮带和空气过滤器都是常见的例子。不同的是，这些零件都是*设计的*，由最终用户或典型的技工替换。

试图声称永久焊接在 PCB 上并埋在仪表板内的球栅阵列芯片是一种磨损物品显然是可笑的。如果是的话，我们会看到一些东西。会有一个建议的时间和里程，eMMC 将被改变，以避免意外故障，这将被列在手册中。此外，特斯拉的维修过程将涉及从电路板上拆下 eMMC 芯片，并直接更换它。鉴于特斯拉将电脑作为一个整体进行更换，这表明该零件*而不是*被任何人、任何地方视为磨损物品。

显然，芯片*可以被*替换，但这并不是一件容易的事情。一旦计算机的主板从汽车中取出，存储器必须备份到 JTAG。然后，[必须小心地回流以移除芯片](https://www.youtube.com/watch?v=-wCaBDUQySI)，这是一个微妙的过程，很有可能会损坏板上的其他组件。如果芯片是一个磨损项目，它不需要专业的 BGA 回流设备来改变。我们会看到泰斯拉经常这样做，替换掉[一个低于 7 美元的芯片](https://www.aliexpress.com/item/1005002007094449.html?src=google&albch=shopping&acnt=708-803-3821&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=UneMJZVf&&albagn=888888&isSmbAutoCall=false&needSmbHouyi=false&albcp=9604210690&albag=100463787298&trgt=374448549250&crea=en1005002007094449&netw=u&device=c&albpg=374448549250&albpd=en1005002007094449&gclid=Cj0KCQiApY6BBhCsARIsAOI_GjZclpNye3yLngs446Vg8Dpi9XHp3dEeZVilKyQoB-qzBnMl-oXY1S0aAk8FEALw_wcB&gclsrc=aw.ds)，而不是以数千美元的代价替换掉整个主板。诚然，现代汽车的某些部件更换起来也很耗时，比如同步带、水泵等等。然而，同样，在这些情况下，汽车制造商提前明确这些是磨损项目，为它们制定维护计划，并制定标准流程来改变它们。

没有人会忍受每次刹车磨损时更换整个前悬架系统——汽车制造商意识到刹车片是磨损物品，并相应地进行设计。特斯拉只是丢了球，对闪存写得太频繁了，这是不容易替换的。合适的解决方案是琐碎的。要么停止将如此多的日志记录到闪存中，要么让它更容易被换出。

并且可能将日志放在它们自己的分区中。虽然 SD 卡可能不符合存储汽车操作系统的标准，但它们可以成为存储可能永远不会被读取的非关键日志的廉价场所。或者，将 eMMC 芯片放在可移动模块上，或者只使用带有汽车级连接器的 M.2 驱动器。

据称，该问题仅影响 2018 年 3 月之前建造的型号，这些型号运行在 NVIDIA Tegra 3 上。后来的型号基于英特尔凌动，并配备了更大的 eMMC 芯片。这些模块尚未证明同样的故障，特斯拉声称他们不应该遭受这个问题。我们走着瞧。