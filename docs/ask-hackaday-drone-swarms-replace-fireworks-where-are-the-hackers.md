# 问 Hackaday:无人机群取代烟花；黑客在哪里？

> 原文：<https://hackaday.com/2019/12/26/ask-hackaday-drone-swarms-replace-fireworks-where-are-the-hackers/>

你妈妈总是警告你那些烟花会把眼睛弄瞎。然而，烟花表演中最热门的新事物根本不是烟火。相反，一群协调的无人机带着不同的灯光效果飞向天空。这使得一些非常惊人的表演成为可能，在半空中展示时完全控制每个光源的方向、颜色和亮度。它还有一个更安全的附带好处——这可能是在社交媒体平台上传播的烟花事故视频结束的开始吗？

为了了解无人机群展示的可能性，请查看该网站上的 ( [机器翻译](https://translate.google.com/translate?hl=&sl=zh-CN&tl=en&u=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2FV4pKVWxOtEejvutq7PwQzw&sandbox=1))惊人图片，它们很好地展示了 3D 效果。请注意，尽管在许多拍摄过程中，摄像机似乎是在移动的，但为了达到类似的效果，swam 本身可以相对于静止的观众进行旋转。

我找不到的是业余爱好空间里发生的很多事情。当然，在美国，限制性的无人机法律可能会妨碍你做这样的事情。但从纯技术角度来看，这似乎并不难做到——至少对于简单的设计来说是如此。此外，在美国领空肯定有一些方法可以做到这一点，因为[无人机表演](https://en.wikipedia.org/wiki/Drone_display)已经在洛杉矶、纽约、迈阿密和加利福尼亚州福尔瑟姆的超级碗上进行。

因此，如果对规章制度进行分类，那么建立一群你自己的表演无人机需要什么呢？

## 空中交通管制的挑战

最困难的部分是保持飞机的紧密队形。根据你想要的紧密程度，GPS 可能就足够了，可以选择差分 GPS 或其他更高分辨率的解决方案。更难的是避免空中碰撞。无人驾驶飞机需要一点空间来纠正意外的速度变化，即使两者之间的小碰撞也可能像三维多米诺骨牌一样在群体中级联。你需要确保它们中没有一个在同一时间穿越相同体积的空间，并有足够的误差来考虑位置不确定性、阵风等等。

根据今年早些时候的一篇文章，[许多公司建立了自己的硬件和软件](https://www.inavateonthenet.net/features/article/the-steep-learning-curve-for-drone-light-shows)，一些公司专注于基于 GPS 的户外展示，而另一些公司则专注于室内展示。那篇文章提到无人机之间的距离可以在 1.5 到 3 米之间。为了帮助解决安全问题，一些公司使用微型无人机，这在机动性方面也很有意义。

我见过一些[设置节目的控制软件](https://www.ugcs.com/)。它支持许多不同种类的无人机，包括相对便宜的 Spark。有一个 [GitHub](https://github.com/ugcs/ddc) 有一些使用它的例子——它显然是使用 Blender 来制作动画部分。当然，也有[的竞争对手](https://www.droneshowsoftware.com/)。

 [https://www.youtube.com/embed/yDdQjc5Oj_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yDdQjc5Oj_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 那么开源在哪里呢？

坦白地说，我对缺乏开源或 DIY 项目感到惊讶。最明显的限制是成本，因为即使一个小的展示也需要几十架无人机，需要建造、储存、运输和测试。但是考虑到一些为黑客阵营建造的大型设施，这并非不可能。对消费级无人机的广泛需求意味着大量现成的无人机既可用又负担得起，而且[已经做了很多工作来对最普遍的型号进行固件逆向工程](https://hackaday.com/2014/12/10/reverse-engineering-the-proto-x-quadcopter-radio/)。

我认为你在软件方面需要的几乎所有东西都已经以某种形式存在了。很明显，Blender 可以做动画。已经有开源的自动驾驶。有一些叫做 [OpenDroneControl](https://github.com/opendronecontrol) 的东西，但它已经有一段时间没有被激活了。

 [https://www.youtube.com/embed/ZbCR8mOPkuo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZbCR8mOPkuo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我错过了吗？有没有一些开源工具至少是简单易用的？或者这是一些黑客项目的成熟场所？请在评论中告诉我们你是否做过群集，以及你是如何做到的。或者，如果你知道任何我们应该知道的工具，也加入进来。