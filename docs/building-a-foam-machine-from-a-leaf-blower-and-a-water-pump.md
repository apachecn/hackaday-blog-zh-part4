# 用吹叶机和水泵造一个发泡机

> 原文：<https://hackaday.com/2019/06/28/building-a-foam-machine-from-a-leaf-blower-and-a-water-pump/>

想象一个充满泡沫浴的浴缸，除了它是一个俱乐部舞池，音乐整夜播放。这就是所谓的“泡沫派对”——一个疯狂而令人兴奋的概念，尽管如此，许多人还没有经历过。20 世纪 90 年代，这个概念在伊比沙岛大受欢迎，世界各地的夜总会和节日都会定期举办泡沫派对。

泡沫是由名为“泡沫机”的设备产生的，任何想举办这种活动的人都可以很容易地购买或租用这些设备。然而，这不是黑客的方式。如果你有点小聪明，注意安全预防措施，以下是你自己可以做到的。

## 发泡机是怎么工作的？

![](img/f2b68370b1e895553bb8433006ec19af.png)

This is a foam party. Yes, you should definitely have one.

如果你吹过泡泡，你会对基本理论很熟悉。在开口处形成一层肥皂膜，然后吹入空气，就有可能形成气泡。

泡沫也是以同样的方式产生的——它只是数以百万计的微小气泡堆积在一起。为了产生泡沫，我们需要同时吹大量的小气泡。我们需要创造一个小得多的东西，成千上万次地并行，而不是用一圈金属丝做成一根泡棒，然后浸在肥皂里。是吹泡泡的 FPGA。

起点是使用织物膜，它将作为气泡产生的表面。然后将薄膜浸泡在肥皂水中。此时，织物变成了覆盖在肥皂膜上的微孔矩阵。然后让空气通过这种织物，数以千计的气泡同时产生，聚结成泡沫。保持空气流通，保持布料湿润，伙计，你就有了一台泡沫机器！

## 实用的方法

制造一台发泡机可能很便宜，也可能非常昂贵，这在很大程度上取决于你已经拥有的材料和硬件。所需的主要部件是一个泡沫锥、一个泵、一个罐和一个气源。本指南只是生产发泡机的一种方法，目的是使用便宜且容易获得的部件。如果你有钱投资这个版本，或者有很多很棒的设备，有其他的途径可以选择，但是这应该会让你朝着正确的方向开始。

![](img/78eb4ad84b16523396e3ef36737cbbf6.png)

The basic layout of a remote-air foam machine. Contrast this to a direct foam machine, where the membrane and sprinkler head are affixed directly to the outlet of the air source.

水箱是一个简单的考虑——它是一个装肥皂水混合物的容器。对于一个 30 人左右的派对，一个 4x4m 的舞池，250 升应该足够了。基本上任何容器都可以使用，从桶到垃圾箱。然而，考虑到人们会在你的泡沫里跳舞，清洁是最重要的。使用一个新的，干净的油箱是最好的——使用一个旧的 44 加仑的油桶可能会让你所有的朋友接触性皮炎，毁了这个夜晚。

 [![Don't underestimate the charm of having a big videogame-style barrel in your front yard. Ours used to store ethanol, and needed a hatch cut for pump installation.](img/96465fec314d5bbd0770f61fe7e3e269.png "vlcsnap-00085")](https://hackaday.com/2019/06/28/building-a-foam-machine-from-a-leaf-blower-and-a-water-pump/vlcsnap-00085/) Don’t underestimate the charm of having a big videogame-style barrel in your front yard. Ours used to store ethanol, and needed a hatch cut for pump installation. [![Sometimes overkill is just easier. Get yourself a big, stout pump and you won't have to worry if it can get the job done.](img/11ce276e64359fe2529302f562feadc3.png "vlcsnap-00079")](https://hackaday.com/2019/06/28/building-a-foam-machine-from-a-leaf-blower-and-a-water-pump/vlcsnap-00079/) Sometimes overkill is just easier. Get yourself a big, stout pump and you won’t have to worry if it can get the job done.

我们用的是一个塑料桶，以前装的是酿酒用的食品级乙醇，用之前洗了几次。这是重量轻，便宜，顶部很容易切断，所以我们可以下降泵。对于泡沫流体，大多数 DIY 构建推荐 2%的肥皂水混合物。这位作者成功地将 5 升水和 250 升水混合在一起。在这里达到最低浓度是至关重要的。很多时间都在想为什么机器不能产生泡沫，直到意识到我们的混合物稀释了 10 倍。

水泵的工作是将肥皂水从水箱输送到泡沫锥，通过喷嘴产生足够的压力使肥皂水雾化。任何一种每分钟能输送 10 升、扬程几米的泵都应该是合适的，但对于外行来说，找到合适的指定泵可能很困难。

在一次流产的洗衣机排水泵实验后，我们决定花 70 美元买一台我们能找到的最便宜的大流量潜水泵。最大流速为每分钟 233 升，其性能对于应用来说是大材小用。然而，当在时间和预算限制下工作时，一次超支比两次欠支划算。作为潜水泵，它也简化了我们的管道。我们不必担心灌注泵和安装配件和软管到水箱，我们只需将泵放入并打开即可。考虑到大多数大型五金连锁店都可以买到便宜的大流量潜水泵，它们是一个安全的赌注，可以完成工作。

![](img/b4967bddfdee9109970e66dea74478e5.png)

The air supply is somewhere you might find it easier to skimp on parts. This would be the first area for improvement if we did a follow-on build.

空气供应是选择变得更加多样化的地方。对于这种应用，需要大量相对缓慢移动的空气，这最有利于产生气泡。您在这里的选择也将影响您的泡沫锥设计。最好的选择是选择一个大型的工业抽风机，这种类型的抽风机通常用在发动机上。这些由安装在圆柱形外壳中的强大风扇组成，通常可以将泡沫锥膜和洒水喷头直接安装在前面，从而降低复杂性。然而，这些风扇相当昂贵，即使在二手市场上。另一个更便宜的选择是使用吹叶机或真空鼓风机。对于我们的构建，我们能够从当铺以每台 5 美元的价格获得两台二手鼓风机 vac。设定他们的真空设置，很容易附加一个管道输送空气到泡沫锥。虽然它们不像大换气扇那样输送大量的空气和泡沫，但就价格而言，它们是制造功能性泡沫机的好方法。哦，他们也很吵。不过，这对赌客来说并不重要——把音响开大，让啤酒源源不断，他们连眼皮都不会眨一下。

![](img/1af405ec5ed3ef6d0c6a5b3313e1bc6c.png)

Fundamentally, the foam cone consists of a water feed and an air feed, stuffed into a bucket, underneath a fabric membrane. Pictured here, one can observe the air inlet pointed down, and sprinkler nozzle pointed up.

泡沫锥是这场表演的明星；这是所有活动发生的地方。织物膜被拉伸穿过一个开口，空气通过该开口吹入。泡沫锥还包含喷嘴，肥皂水通过喷嘴喷到薄膜上，以保持薄膜湿润并随时产生泡沫。

制作泡沫筒的一个简单方法是将一件旧的棉 t 恤在桶的开口处拉伸，然后用拉链固定住。然后可以钻孔，以允许水管进入水桶并安装喷嘴，以及用于空气供应的大管入口。这两个孔都应该密封好，以确保所有进入泡沫锥的空气都通过薄膜排出。任何孔洞都会减少用于制造泡沫的空气量。

![](img/997bfa2966252fef0ebc31bfd68f550a.png)

This table was built with a slot in the middle to allow air and water hoses through. Note the tap on the water line, allowing the water to be shut off in the event of malfunction.

顺带一提，其实把喷头对准膜并不是超级重要的。在一个密封良好的泡沫锥中，任何进入的水都无处可去，只能从膜中流出，所以涌入的空气会以某种方式将水带到那里。在我们的设计中，我们将空气软管安装在铲斗的侧面，使其通过一个 90 度的弯管吹向底部。这迫使气流转过 180 度到达出口，减慢气流速度，帮助气流发展到铲斗的全直径。这一点很重要，因为我们的叶片鼓风机产生的气流是一股小而快的射流；为了产生好的泡沫，我们需要更慢、更宽的气流。然后，我们在水泵供水的水管末端安装一个小型灌溉喷头，也从侧面供水。然后用胶带和强力胶将桶密封起来，泡沫锥就可以使用了。

把所有这些部件连接起来，你就有了一个正常工作的发泡机！

## 安全考虑

使用发泡机时，安全是一个重要因素。在任何结合水电的钻机中，必须采取预防措施以避免触电死亡的风险；[如果没有给予应有的考虑，后果可能是悲惨的](https://www.jpost.com/Israel/2-brothers-killed-in-Antalya-foam-party-tragedy-laid-to-rest)。

![](img/6ac1b48336d3080d2bc9036c27a45ce5.png)

Placing the leaf blowers inside a cabinet reduced noise, but also increased operating temperatures. This was closely monitored to avoid fire.

发泡机的制造方式应确保电气部件和电缆不会接触到水或泡沫。无论是在正常操作中，还是在发生泄漏或故障时，都应该如此。墨菲定律告诉我们，哪里出错了，哪里就会出错，因此机器的设计应该是安全的，即使在出现故障的情况下。在我们的设计中，通过使用适当额定的潜水泵，输水系统可以被认为是电气安全的。来自吹叶机的空气也通过管道输送到泡沫锥，使它们远离水和泡沫。吹叶机也被抬高到离地面很远的地方，确保它们在泡沫增加时保持干燥。为泡沫派对选择的房间是一个厨房，厨房里没有地板上的电源插座，这些插座可能会在不经意间被打开并造成危险。房间内的所有出口都在高处，泡沫保持在该高度以下，以避免与液体发生电接触。

安全也是关于操作程序的。在我们的聚会上，发泡机只能在严格的监督下运行有限的时间。这意味着，如果有泄漏或火灾，有人在手边随时准备关闭机器。多个人被告知在发生火灾或其他故障时该做什么。这包括让小组熟悉灭火器的位置和房子的配电板，以防接近机器关闭机器变得不安全。

诀窍是采取适当的预防措施，以便安全地做危险的事情。

## 不不不是的。

![](img/304bd387099c56a3c80c23c3b1616482.png)

Later improvements came by mounting the foam cones flat on a table, rather than hanging from a frame as pictured. This improved foam production significantly, though we are not sure why.

每当你在建设一个涉及水的项目时，很有可能会出现漏水。我们面临着软管从倒钩上滑落，水管上有洞，甚至水箱因为水泵缺少截止阀而被虹吸出去。这让我们随着时间的推移改进了设计，在管道的几个地方安装了水龙头，以便在发生泄漏时能够快速关闭管道。这意味着，在一个喧闹的派对过程中，当我们的软管在中途完全爆裂时，我们只洒了 50 升液体。这也允许调节泡沫锥的流速，以帮助最大化泡沫产量并避免任何溢出问题。

这位作者愿意花一年时间研究生产最佳泡沫所涉及的流体力学和工程因素；如果你有建议，一定要在评论中分享。

![](img/220f435b1a811b0d4d1d8041d2bd7a2e.png)

Quite literally, good clean fun.

在这样的项目中，永远不要低估让他人参与进来提供帮助的价值。让周围的人去取工具并提供不同的观点可以使故障诊断更快。人们也可以带来不同的技能。由于一位经验丰富的农场工人的帮助，我们的项目变得更加稳健，他向我展示了如何通过使用水壶更好地将管道安装到带刺的配件上。另外，泡沫和朋友在一起总是更有趣！

总的来说，对于有经验的黑客来说，很容易就能制造出一台泡沫机，举办一场史诗般的派对，而且我们可以通过实验证实，加入泡沫会让任何舞池的受欢迎程度提高 300%。祝你好运，当你完成那个甜美的泡沫建筑时，你知道该给谁打电话。黑客快乐！

 [https://www.youtube.com/embed/l0Jxm3YYhj0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l0Jxm3YYhj0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

