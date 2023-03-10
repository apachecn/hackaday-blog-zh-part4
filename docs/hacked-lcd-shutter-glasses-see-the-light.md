# 黑掉的液晶快门眼镜见光

> 原文：<https://hackaday.com/2018/07/12/hacked-lcd-shutter-glasses-see-the-light/>

看到一个大的消费技术失败，总会有点难过。但当然，对我们这些黑客来说，好处是由此产生的大甩卖通常是硬件的绝佳来源，否则很难得到。3D 电视是最新抵达这个不受欢迎的消费科技之岛的产品。有那么一小段时间，电视制造商几乎让人们相信，坐在客厅里戴着又大又傻的电子眼镜是一个可行的解决方案，但最终我们知道结果如何。

那些老掉牙的眼镜现在只需原价的几分之一就能买到，而且黑客攻击的时机已经成熟。[凯文·科斯特]一直在摆弄它们，[他最近想出了一个电路，为佩戴者提供了一个独特的世界视角](http://computernerdkev.heliohost.org/rainbowglasses/index.htm)。任何反射表面都会看起来像是辐射彩虹，他承认这在静态图像中不会显示得很好，但看起来足够酷，他认为值得将板投入生产，以防其他人想参与折射行动。

为了解释它是如何工作的，我们需要后退几步，看看这种类型的眼镜中使用的 LCD 面板的机械结构。冒着过于简化的风险，人们可以说液晶显示器有点像电容器:当充电时，晶体以这样一种方式排列，从而改变了通过的光的偏振。结合外部偏振滤光器，最终结果是使面板变得不透明。为了把晶体放回原来的位置，让光再次通过，LCD 面板被短路，就像你对电容器放电一样。

[凯文]发现，如果他让液晶面板慢慢放电，而不是完全短路，它会逐渐淡出，而不是立即变得透明。他的理论是，这种部分偏振导致了彩虹效应，因为穿过佩戴者眼睛的光处于“扭曲”状态。

[Kevin]提供了构建您自己的“彩虹适配器”所需的所有信息，但是您也可以从 Tindie 购买套件或组装板。如果你正在寻找其他项目来利用那些收集灰尘的 3D 眼镜，那么[将它们变成自动太阳镜](https://hackaday.com/2012/11/14/turning-3d-shutter-glasses-into-automatic-sunglasses/)或者尝试一下[治疗你的弱视](https://hackaday.com/2018/03/13/hacked-3d-tv-glasses-may-cure-lazy-eye/)怎么样。