# 每只耳朵都有一圈发光二极管

> 原文：<https://hackaday.com/2021/04/17/a-halo-of-leds-for-every-ear/>

很少有什么能像一束束微小的发光二极管一样让普通员工兴奋。越小越密越好，任何形式都可以，只要我们能得到一个微距镜头或一个流畅的动画视频。这一次，我们请来了[Sawaiz Syed]和[Open Kolibri]为我们带来明亮的商品，以及极小的 [HALO 90 反应式 LED 耳环](https://openkolibri.com/hlo/90/)。

HALO 90 的设计目的是作为耳环，尽管我们怀疑它们也可以作为很好的胸针、发饰或桌面物品。为了达到这一目的，每款手机的直径只有 24 毫米，使用 CR2032 电池的重量只有 5.2 克(仅 PCBA 手机就只有 2.1 克)。从功能上讲，他们目前的软件包括三种动画模式，每种模式都可以通过设备上的一个按钮来选择；音频反应、光晕(完全照亮)和闪光。查看文档了解每种模式下预期电池寿命的细节，但可以说，无论如何，这些耳环都可以度过几个夜晚。![](img/683f370bc34cda3b0626a67e557a1531.png)

就硬件而言，HALO 90 就像你预期的那样简单。每个设备都由 STM8 以最大 16MHz 的速度驱动，即使进行实时音频处理，这也足以让 90 个 charliplexed 0402 LEDs 以 1kHz 的更新速率嗡嗡作响。事实上，这里的 [BOM](https://github.com/openKolibri/halo-90/blob/master/readme.md#bom) 非常简单，只有 8 个组件；led、微控制器和麦克风、电池座和无源器件以及按钮。[Sawaiz]甚至设计了一个特别光滑的盒子来搭配每对耳环，它可以容纳两个 HALO 90 和两个 CR2032，并包括一个磁性闭合，以实现最令人满意的盖子动作。

正如他的一些其他作品一样，[Sawaiz]已经为[制作了大量与 HALO 90 相配的特殊文档](https://github.com/openKolibri/halo-90/blob/master/readme.md)。这些文档可以直接从他那里获得，完全组装好，但有了这么好的文档，通往家庭建筑的道路应该是光线充足且容易接近的。他甚至选择了着眼于长期可用性、低成本和易于采购的零件，因此无论您何时决定开始，都应该是轻而易举的。

很难从[Sawaiz]迷人的收藏中选择几幅图片，所以如果你需要更多的休息后在扩展集上大饱眼福。

![](img/1bbf4d3bb965036ad54e169beb75dac9.png)

HALO 90’s in their cases, ready for a night out

![](img/e15f688e9512bc04c025d5a49ef0f97d.png)

Even the panel is aesthetically pleasing