# 采访:斯图亚特·森普尔谈彩通、自由色调、色彩和开源

> 原文：<https://hackaday.com/2022/11/16/interview-stuart-semple-on-pantone-freetone-colour-and-open-source/>

我们最近报道了从 Adobe 云产品中移除 Pantone 颜色支持的消息，这两家公司现在希望艺术家和设计师为 Pantone 插件支付额外的订阅费，否则他们的 Pantone 颜色的作品将被黑块淹没。我们的报道集中在我们的社区，以及一个试图主张颜色所有权的商业实体的荒谬性如何不会对我们的三字节 RGB 值产生影响。

## 采访一位艺术家和颜料活动家

[![Freetone, 1280 liberated colours, Stuart Semple](img/c66b4a82ec02821c07b88ade99d6ee6f.png)](https://hackaday.com/wp-content/uploads/2022/11/FREETONE_WHITE.jpg)

The palette that could start a revolution.

公平地说，尽管我们关注硬件黑客和开源爱好者，但我们忽略了它对艺术家和设计师的影响。为了纠正这一遗漏，我们需要走出我们的领域，与一位艺术家交谈，在这种情况下，显然需要采访一个人。

斯图亚特·森普尔可能是当代英国最著名的艺术家之一，但与这个故事相关的是，他在颜色和知识产权问题上的激进主义让他成为了权威。他通过发布自己的艺术材料引起了人们对这个问题的关注，这些材料的颜色直接挑战了那些公司试图为自己主张的颜色，也许在我们的社区中最出名的是[挑战安尼施·卡普尔对 VantaBlack](https://hackaday.com/2018/01/25/the-current-state-of-the-black-market/) 的独家许可，所谓的“世界上最黑的颜料”。

最近，为了回应 Adobe/Pantone 的争议，他发布了一款 Adobe 套件的免费插件 [Freetone](https://culturehustle.com/products/freetone) ，用其网页上的话来说，该插件包含*“1280 种解放的颜色极具 Pantoneish 风格，让人想起有史以来最具标志性的色彩手册中的颜色。事实上，有人认为他们与 Adobe 付费墙背后的人没有什么区别。我和他通了电话，他解释了为什么 Freetone 会出现。*

我知道 Pantone 是设计师使用的东西，所以我过去曾为一些公司工作过，这些公司的设计师会指定一个 Pantone 索引，它会以相同的方式出现在屏幕上、打印框上以及其他任何地方。但是为什么你作为一个艺术家为什么要用 Pantone 呢？

[![A rack of test tubes of blood-red paint](img/62b199eda7e333735fd47dd235bf6067.png)](https://hackaday.com/wp-content/uploads/2022/11/stuart-semple-gay-blood.jpg)

Art, activism, and a very red pigment.

嗯，我在很多方面都用它。所以我做了很多丝网版画作为我艺术的一部分。所以你知道，如果我用丝网印刷机工作，我想知道他们对我的作品所做的印刷是我想要的颜色，所以 Pantone 对我来说真的很有用。

但是，即使是在颜料里，我也做了一些颜料，[实际上使用了同性恋者的血液。对我来说，颜料的颜色和真正的血液颜色相匹配是非常重要的。所以我和很多人一起工作，我们一直在合作，我和一些在纽约的朋友一起工作，我们需要一个共同的语言。](https://culturehustle.com/pages/the-gay-blood-collection)

我所说的红色就是他们所说的红色，而 Pantone 在这方面非常有用。事实上，这是最重要的。我刚刚为 Placebo 乐队做了一张唱片封面，这是一家印刷公司为我制作的，所以我必须告诉他们我想要什么样的专色。所以我不得不告诉他们潘通参考，这是他们理解的语言。

所以我的下一个问题与 Freetone 有关。显然，正如你发布的那样，它是一个 Adobe 插件。它是如何解决问题的？因为很明显，我可以指定一种自由色调的颜色，任何有自由色调的人都可以说是的，就是这种颜色。但是，我如何去找一个购买了 Pantone 规格墨水的印刷商，并把它们一一对应起来呢？

[![An open Pantone swatch book in a fan](img/7ea0ae9e303d22e255229cb4aa5cc36a.png)](https://hackaday.com/wp-content/uploads/2022/11/Nuancier_Pantone_2_Cut_out.jpg)

The Pantone swatch book which you’ll see in the hands of artists and designers everywhere. Céréales Killer [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:Nuancier_Pantone_2_(Cut_out).jpg).

它的工作原理是，如果你下载 Freetone，你会在里面找到各种颜色，其中一种叫做 Sempletone 648C。嗯，和 Pantone 648C 一模一样。如果你在屏幕上工作，使用 Freetones，然后当你把它发送到打印机，它实际上是明显的，任何人都清楚地看到 648C。如果你有潘通风扇的书，你看看颜色，它是一样的。我的 846C 和风扇里的 846C 是一样的，在潘通的书里。我想看到他们试图争辩说他们拥有它，但我不认为他们在名称或 Pantone 商标上拥有它，但这些是带数字的 Sempletones。所以我觉得会很难。

我的下一个问题可能是更深入地了解这一切的技术。你认为有可能完全取代 Pantone 的服务吗？所以，如果你把每一种颜色都拿到分光计上，然后公布光谱，你能对墨水制造商或类似的人说，这是全部的技术细节，而不仅仅是一种颜色，你的颜料符合这个光谱吗？我很好奇在这方面你能把开源推进到什么程度。

[![PySpectrometer version 2, showing mini spectroscope, 4 inch display and hand for scale](img/e9f4d46704f96bccf539082f71124863.png)](https://hackaday.com/wp-content/uploads/2022/10/9630161666475439796.png)

The PySpectrometer project, something for anyone with an interest in colour.

斯图尔特那真的很酷。我喜欢它。比如，如果你能给他们光谱数据，如果他们有光谱仪，他们可以在他们的末端测量。但是目前还没有什么先进的东西，很多动作还是靠眼睛来完成。我的回答是，如果有足够酷的设备，我看不出有什么不可以。我不知道分光计是否能匹配它。我不明白为什么不，我不明白为什么你不能公布数据。但是它必须是整个光谱信息，而不仅仅是一个 RGB 值。

(*在这一点上，采访暂时偏离了对开源光谱仪的讨论，例如[我们最近报道的 Raspberry Pi 项目，](https://hackaday.com/2022/10/29/pi-based-spectrometer-gets-an-upgrade/)因为 Stuart 哀叹光谱仪可能是一种极其昂贵的仪器。采访者的工作不是引导他们的被采访者，所以我们跳过了文字记录的这一部分，但是我认为我们都可以期待 Stuart 对一个负担得起的光谱仪的任何使用。我们将在下一个问题中继续采访。*)

[![Photoshop Pantone warning popup.](img/2bcb32a627685a20c0d30facee29c65a.png)](https://hackaday.com/wp-content/uploads/2022/11/adobe-pantone-message.png)

This widely shared screenshot represents the destruction of past work.

整个 Adobe 套件的一个真正问题是，这种情况在世界范围内也发生过，例如 Autodesk CAD 软件包，它们已经进入了云端，成为了订阅软件。所以我完全理解艺术家们在突然被告知他们必须支付额外的订阅费才能保持对 Pantone 的支持时的沮丧，我特别震惊地发现 Photoshop 不仅在 Pantone 颜色上显示黑色像素，我被告知它在保存时删除了 Pantone 信息。作为一名艺术家，你认为开源软件生态系统中的任何东西都有可能取代像 Adobe 套件这样的专有产品吗？

是的，100%，有很多东西。我认为开源就是答案，我相信自由。自由意味着表达自己的自由，拥有事物的自由，发微博的自由，改变事物的自由，以及其他的自由。所以是的，百分之百。我认为实际上有比 Photoshop 更好的东西，我们的问题是 Adobe 垄断了行业。如果你想和某人一起工作，你必须会说那种语言。这仍然是个问题。它就像一个操作系统，但是它有垄断权。

所以还有其他东西，例如，在 Mac 上，有一个叫做 [Pixelmator](https://www.pixelmator.com/pro/) 的东西，在我看来，它和 Photoshop 一样好，我每天都在用它。不是免费的，但是你买一次，就这样，免费更新。就像以前的软件一样。还有其他的，比如 GIMP 很神奇。很牛逼，但并没有真正取代 Photoshop。

[![A screenshot of GIMP](img/75771aa3d54f4d448e9b06fc6ddb49fc.png)](https://hackaday.com/wp-content/uploads/2022/11/gimp-windows_crop.jpg)

We all like using GIMP, perhaps other people could learn to love it too. ([gimp.org](https://www.gimp.org/screenshots/))

在 Hackaday 上，我们可以大声疾呼，如果 GIMP 或其他软件的开发者能够将 Freetone 嵌入他们的产品中，那该有多好，因为他们没有得到许可的 Pantone？

是的，那会是一个梦想，不是吗？我是说，为什么不呢？我为每个人做的。就我而言，它就在那里，利用它，改变它。融入吧，人越多越好，我觉得。

很多人用 GIMP，它很好。一直以来都是非常好的开源软件。我们知道未来是在开源的东西，专有的东西不会持久，它只是不适应。这是把贪婪和利润放在用户之上，是行不通的。没有自由可言。

对我来说，最令人震惊的事情是，据我所知，他们将从你的 PSD 中删除 Pantone 信息。这真的让我震惊。

他们真的拿它当人质。大概 20 英镑，或者从你的作品里删掉，哇。反正他们不会给我任何东西。我在租软件，每个月付费使用软件，不是免费的。而且牌照费很多。我们已经在这个软件上一年花了几百上千英镑，大概一年 800 英镑。另外 20 英镑，只是为了完成我们之前的工作。我是说，这是我们的工作！这纯粹是公司的贪婪，不是吗？

非常感谢您的面试。

当我们结束时，我问他关于他的[黑色 3.0 颜料](https://culturehustle.com/collections/black)，这是对万塔布莱克和安尼施·卡普尔的反应。我很好奇它是否对头部挂钩或太阳能收集器有特别好的红外响应，但遗憾的是，他告诉我这主要是艺术家的视觉颜色。这是非常酷的东西，令人难以置信的黑色，我真的想得到一些玩，但可能不会比一个拨浪鼓可以热的目的。没关系，工程师的好奇心得到了满足。

## 艺术家和工程师的下一步是什么？

[![Swatchbooker screenshot](img/a640da8cc91c6c7661ebe044c108a9d4.png)](https://hackaday.com/wp-content/uploads/2022/11/SwatchBooker-0.7.png)

Could [SwatchBooker](http://www.selapa.net/swatchbooker/) hold the answer?

采访之后，值得从我们和他的角度来看一下 Freetone 项目。如果我们作为一个社区想要确保颜色不会变得越来越专有，那么我们可能有责任确保在我们的范围内适当地支持它。例如，GIMP 支持将一举使开源软件成为数百万艺术家和设计师更容易的选择，我认为通过其现有的调色板支持可以相对容易地做到这一点。有 [SwatchBooker](http://www.selapa.net/swatchbooker/) 似乎执行必要的交换，我发现了 [ASE2GIMP](https://github.com/RoyCurtis/ASE2GIMP) 项目，它将 Adobe 调色板导入 GIMP，但遗憾的是我不能让它在这里工作。如果 GIMP 附带了一个内置的 Freetone 调色板，那会不会是一个难以想象的开发任务？

从 Stuart 的角度来看，在坐下来玩了 Freetone 之后，如果有一件事我可以问他，那就是把它不仅仅作为一个 Adobe 插件来发布，并且给它一个开源许可。按照现在的情况，这是一个可以通过他的网上商店免费获得的二进制文件，我认为将其作为一个简单的列表发布，甚至可能像一个 CSV 文件一样简单，会让开发人员更容易访问它。再加上允许他们将它包含在软件中的开源许可，我认为这是不可分割的。在 Hackaday，我们不是开源许可的书呆子，但是我猜想像 LGPL 为图书馆做的那样为调色板做同样的事情是合适的。

在我们的世界里，我们被电子产品和代码包裹着，有时很容易忘记我们所做的工作远远超出了我们的工作台。如果你在黑客空间呆了足够长的时间，你会知道艺术和工程几乎是同一个硬币的两面，所以发现这样的交叉时刻是令人高兴的。让我们希望 Freetone 的支持能够融入到开源运动中，并且我们一起能够阻止另一场知识产权争夺战。