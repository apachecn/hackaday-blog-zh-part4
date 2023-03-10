# 厨房里的机器学习可以做出美味的混搭甜点

> 原文：<https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/>

一级防范禁闭期间你做了什么？很多人在去商店寻找卫生纸和洗手液的间隙转向烘焙。他们中的许多人出于某种原因烤面包，但像我们一样，[萨拉·罗宾逊]转向更甜的东西来度过难关。

[![](img/489aacc48dd99501bcb7827060261487.png)](https://hackaday.com/wp-content/uploads/2021/01/sarah-cakie.png)

The first Cakie ever made. Image via [Google Cloud](https://cloud.google.com/blog/topics/developers-practitioners/baking-recipes-made-ai)

她在疫情的思考进入了烘焙存在主义问题的领域，比如，直截了当地说，是什么将烘焙食品区分开来？饼干的松脆、蛋糕的松软和面包的蓬松背后的科学原理是什么？

作为谷歌云的开发者支持者，[Sara]转向机器学习来找出为什么饼干会碎。她收集了饼干、蛋糕和面包的 33 种配方，并建立了一个张量流模型来分析它们，结果得出了一组百分比中每种配方的饼干/蛋糕/面包谱系。该模型不仅能够根据类型准确地对食谱进行分类，[Sara]还能够使用该模型得出一个 50/50 的饼干蛋糕混合食谱。人工智能提供了一份配料清单，她在其中添加了香草精和巧克力片来调味。从那以后，她不得不即兴发挥，为蛋糕想出自己的烘焙方法。

## 从数据表到餐桌

【2020 年 12 月，[Sara]与谷歌的应用人工智能工程师[Dale Markowitz]合作，构建了配方预测器的 2.0 版本。他们还想出了一个饼干面包混合配方，他们称之为 Breakie。

这一次，他们通过收集大约 600 种食谱，建立了一个更大的数据集。为了公平竞争，他们将所有的食谱缩减为 16 种基本成分:酵母、面粉、糖、鸡蛋、脂肪(任何类型的油)、牛奶、小苏打、发酵粉、苹果醋、酪乳、香蕉、南瓜泥、鳄梨、水、黄油和盐。

[![](img/d54d7dd90819e7e4ece8f862c0985697.png)](https://hackaday.com/wp-content/uploads/2021/01/feature-importance.png)

Feature importance of the essential ingredients in baked goods. Image via [Google Cloud](https://cloud.google.com/blog/topics/developers-practitioners/baking-recipes-made-ai)

关键是要包括影响质地和稠度的成分，而不包括不影响的成分，比如肉桂。他们还把所有东西都转换成盎司，并把一些东西挪来挪去，主要是把香蕉面包和南瓜面包之类的食谱移到蛋糕类(它们应该在的地方)。

这一次，这个模型包含了可解释性。机器学习中的可解释性相当于使模型更容易解释，并理解它们为什么做出预测。这是找出饼干与蛋糕和面包的区别的基础。[Sara]和[Dale]使用了谷歌的 [AutoML Tables](https://cloud.google.com/automl-tables) ，这是一种基于表格数据建立模型的无代码机器学习工具。他们输入了一个 CSV 文件，并做了和以前一样的事情——AutoML 分析了每个食谱的成分，并根据成分及其数量判断它们是饼干、蛋糕还是面包。

AutoML 做的一件很棒的事情是计算“与目标的相关性”。在这里，目标是他们试图预测的任何烘焙食品:饼干、蛋糕或面包。每一类的最大预测者是黄油、糖、酵母(如果有的话)和鸡蛋的数量。对于这位业余面包师来说，这些结果很有趣，但并非完全出乎意料——食谱中的鸡蛋越多，越有可能是蛋糕。你曾经用酵母做过饼干或蛋糕吗？这并不是完全没有听说过，但它也不是真正的规范。

## 科学烘焙:蛋糕

我对这些人工智能创造的甜点混搭非常感兴趣，所以我不得不尝试一下。我在 Hackaday 测试厨房点燃了烤箱，开始烘烤。对于第一个实验，我决定制作蛋糕-饼干混合食谱，因为它听起来比“面包灵感饼干”稍微好吃一些。

[![](img/f0f075a8db26ba3fa4bef89446ea52bf.png)](https://hackaday.com/wp-content/uploads/2021/01/cakie.png)

The dessert you didn’t know you needed — a perfect cross between chocolate chip cookies and cake. Image via [Food & Wine](https://www.foodandwine.com/news/google-ai-invents-new-dessert-recipes-cakie-breakie)

我尽可能地遵循食谱，使用室温黄油。在做了一些研究后，我决定把鸡蛋也放在柜台上。我的研究表明，黄油的温度应该是 65 华氏度(18.33 摄氏度)，大约需要四个小时才能加热到可用的温度。

我确实改变了一件事就是锅。谁有 6 英寸的蛋糕烤盘？不是我。我甚至在杂货店都找不到锡箔纸，所以我用了一个 9 英寸的圆形不粘锅，并按照指示涂上油脂。我觉得 25 分钟听起来有点太长了，所以我从 20 分钟开始，然后在我的牙签没有干净时增加了两分钟。这被证明是非常正确的，所以如果你要做这些(你肯定应该做)，在一个 9 英寸的圆锅中做大约 22 分钟。相信牙签测试。

一旦蛋糕从烤箱里拿出来 10 分钟，我就开始吃。正如你所看到的，它像饼干一样碎掉了，并且有一层薄片状的顶层，这是因为糖的缘故。我觉得味道很棒，我老公也同意。它尝起来就像是曲奇和蛋糕的完美结合，不知何故兼具了两者的口感。当我后来回去拿更多的时候，它就更好地结合在一起了。

 [![Somewhere between cake batter and cookie dough.](img/ad2f11f5dc1c39aa6e6e382ef6929940.png "01-cakie")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/20210120_122744_hdr/) Somewhere between cake batter and cookie dough. [![Starting to look delicious.](img/72d9e080acfb7bb88a1a3910234f7722.png "02-cakie")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/20210120_124222_hdr/) Starting to look delicious. [![The toothpick came out clean after 22 minutes.](img/c748525f06447a38275b3ab9ec6e72f4.png "03-cakie")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/20210120_130906_hdr/) The toothpick came out clean after 22 minutes. [![I tried to eat it warm, and the top layer gave way.](img/37afb775ab8081394b09b8d3315622e3.png "04-cakie")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/20210120_131104_hdr/) I tried to eat it warm, and the top layer gave way. [![Crumbles like a cookie.](img/c5b38642e2ab4277bb9e3f2e830b58a6.png "05-cakie")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/20210120_131353_hdr/) Crumbles like a cookie. [![Eats like cake.](img/8bd0499b527a49712dcd5b64f2d4da87.png "06-cakie")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/20210120_141957_hdr/) Eats like cake.

## 他们是早餐

[![](img/43db01c0dfbf311ae598acc57942a228.png)](https://hackaday.com/wp-content/uploads/2021/01/breakie.jpg)

“Bread-inspired cookies” is better than it may sound. Image via [Google Cloud](https://cloud.google.com/blog/topics/developers-practitioners/baking-recipes-made-ai)

第二天，我做了早餐。继前一天的成功之后，我在上午 9:00 把黄油和鸡蛋放在柜台上，下午 1:15 左右开始烘烤。

这个食谱还有一点，正如你在说明中看到的，它被清楚地分为“面包部分”和“饼干部分”。尽管如果你仔细想想，巧克力曲奇的制作方法是一样的——你在一个单独的碗里混合干的原料，然后逐渐加入黄油、红糖、白糖、鸡蛋和香草的奶油混合物中。碎面包以同样的方式组合在一起，尽管面团最终变得很厚——更像面包而不是饼干。

[![](img/b052e3d512393e1263deb6985c34b9f0.png)](https://hackaday.com/wp-content/uploads/2021/01/sarah-breakies.png) 

【萨拉】和她的早餐。看到他们有多可怜了吗？图片 via [Google Cloud](https://cloud.google.com/blog/topics/developers-practitioners/baking-recipes-made-ai)

进去的时候我对自己说，吃完这些早餐后我袖手旁观了一下——酵母不属于饼干。饼干使用小苏打发酵是有原因的，就像快速面包一样。并不是说我能尝出它们里面的酵母，但我觉得肯定影响了质地。

尽管如此，早餐的味道还是很不错的。它们有燕麦葡萄干或糖饼干的口感——非常有质感。我发现酵母很难溶解在规定量的牛奶中，这可能是为什么我的上升没有像[萨拉]的那样令人印象深刻。这也可能与我使用的牛奶有关，牛奶中添加了乳糖酶，用于乳糖不耐受者。也可能是我在微波炉里加热不够。

就像蛋糕一样，热的早餐会分崩离析，但冷的早餐会更好地保持在一起。我有一个刚出炉的(和你一样)，我想我更喜欢冷却的。现在，它们有了一种可以咬进去的脆外壳。

 [![It was already thick before I ever added any flour.](img/ef291345f2de7342f4566b275c28d09e.png "01-breakies")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/01-breakies/) It was already thick before I ever added any flour. [![Seriously, I thought there was no way it would absorb all the dry ingredients.](img/74ca02a7449c6fc3ba0d3d0ebad2a5c3.png "02-breakies")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/02-breakies/) Seriously, I thought there was no way it would absorb all the dry ingredients. [![I managed to get it all mixed in anyway.](img/700d453532f6cf4c00f31b09468b8f63.png "03-breakies")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/03-breakies/) I managed to get it all mixed in anyway. [![The dough balls went flat right away.](img/7a535538e49731dafd8e94246211b608.png "04-breakies")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/04-breakies/) The dough balls went flat right away. [![They're about as thick as regular cookies.](img/648bab315d8f202059494adde72aa09f.png "05-breakies")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/05-breakies/) They’re about as thick as regular cookies. [![You can sort of see the texture here.](img/dd511ab912f87195184cf1e0e1e7dc2c.png "06-breakies")](https://hackaday.com/2021/02/03/machine-learning-in-the-kitchen-makes-for-tasty-mashup-desserts/06-breakies/) You can sort of see the texture here.

总而言之，我认为这个实验是成功的。我认为，最终我们可以也应该相信人工智能会给我们美味的混搭甜点，如果没有其他东西的话。就我个人而言，我有兴趣通过混合馅饼食谱来做更进一步的实验。布丁饼干很好吃，为什么不吃派饼干呢？