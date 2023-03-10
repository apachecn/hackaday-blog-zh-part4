# 如何只用手工工具制作电动滑板车链轮

> 原文：<https://hackaday.com/2019/10/21/how-to-make-an-electric-scooter-chain-sprocket-with-nothing-but-hand-tools/>

有时，机械零件可能会非常昂贵，或者完全没有。在这种情况下，只有一个选择——自己做。正是在这种情况下，我发现自己。我的电动滑板车被一个速度更快的竞争对手略胜一筹，我需要救赎。一个齿轮变化将做到这一点，但唉，链轮我需要的根本不存在从通常的网上分类广告。

因此，我抓起我仅有的工具，忙于我的工作。这是一个可以被任何熟练使用打印机、电钻和旋转工具的人复制的构建。我们开始工作吧！

## 入门指南

![](img/38f065093aebf210198fdaf575bf1c23.png)

The mounting hole geometry was checked against eBay listings for similar sprockets, as well as the original part on the scooter.

![](img/0936b7b133a20fc8379c009d3b447b7b.png)

A list of common chain sizes and specifications. Source: Electric Scooter Parts

制作一个链轮很简单——打印一个模板，把它粘在一块金属板上，然后剪下来。需要一些后期处理，但基本概念与任何基本的木工或工艺项目没有什么不同。

制作一个模板很简单，使用一个叫做 [Sprocketeer 2.0](http://www.idleamusements.com/?page_id=54) 的免费软件。链轮实际上具有非常复杂的几何形状，旨在使链传动尽可能安静、平稳和高效地运行。你所需要的只是你选择的链条的节距和滚子直径，以及你想要的链轮的齿数，Sprocketeer 就会生成轮廓。

我正在为 T8F 链条生产链轮，谷歌搜索为我找到了相关尺寸:8 毫米节距，4.7 毫米滚子直径。我还知道我想要一个 19 齿链轮，以便达到我想要的最高速度。将这些数字输入软件后，我得到了一个 DXF 的文件，我可以将它导入 Inkscape。从那里，我添加了椭圆形安装的几何形状，我可以从易贝类似链轮的列表图像中抓取。完成后，在一张 A4 纸上打印出模板就很简单了。在提交到构建的下一个阶段之前，我仔细检查了最终结果的大小是否准确，这很简单，因为我知道椭圆的确切尺寸。

## 那是很漂亮的金属

![](img/ee04d9c67943d4d13f9824590a6734cc.png)

A post support supplied the metal for this project, but if you can source better stock, use it.

接下来，你需要一些金属来制作你的链轮。低碳钢是一种典型的选择，具有工作所需的韧性，同时还便宜且易于加工。与更硬的钢相比，它们也更有可能更好地磨损，这一点我们将在后面重新讨论。

我的选择有限，因为我只想做一个直径约 60 毫米、厚 4 毫米的小链轮。我能找到的最接近的是 75 x 50 毫米，3 米长，价格昂贵。由于足智多谋，我找到了一个镀锌支柱，只需 10 美元，我就可以把它切开，尽管它只有 5 毫米厚。这将需要一些进一步的工作，但会做得很好。

## 切碎它！

一旦你得到了你的纸模板，这是一个简单的问题，粗糙的金属，并将其附在表面上用强力胶。然后你就可以开始切割了。一个好的方法是首先用角磨机进行长直切割，粗略地勾画出链轮的大致形状。一旦你有了一个大致呈八角形的坯料，就开始在牙齿之间的缝隙处进行切割。在这个阶段，重要的是要保守，不要超过模板的线条。我用研磨机在模板的两边进行小的切割，结果得到了非常粗糙和过大的牙齿——精细是在后面。

![](img/e594a553632bd7e70845961d28ffe67a.png)

With the template glued on to the blank, an angle grinder is used to rough out the basic shape.

![](img/a29b35bd0b1d34f74ccb2f76b5e5ac1c.png)

Using a rotary tool is an easy way to route out the center mounting hole.

这是在链轮中心粗切安装孔的好时机。根据链轮的安装方式，您可能需要使用不同的技术。电钻通常是开始的好方法。如果你想要一个椭圆形或 D 形的安装孔，像 Dremel 这样的旋转工具是一个很好的加工方法。我一开始用的是一把 [561 多功能切割钻头](https://www.dremel.com/en_US/products/-/show-product/accessories/561-multipurpose-cutting-bit)，然而当我们切割钢材时，像 [9903 切割器](https://www.dremel.com/en_US/products/-/show-product/accessories/9903-tungsten-carbide-cutter)这样的碳化钨钻头是一个更好的选择。

![](img/56468d28d5511f000964068a38e843fe.png)

Using a power drill as a lathe can be dangerous; be sure your set up is mounted securely.

在进一步切割齿之前，我需要减薄链轮毛坯。T8F 的滚子宽度为 4.8 毫米，但大多数链轮只有 4 毫米厚，逐渐变细至约 2.5 毫米，以使它们与链条平滑啮合。我的毛坯有 5 毫米厚，这根本不行。这是车床的工作。令人欣慰的是，只需要一个电钻和一个 G 形夹就可以轻松制作自己的车床。

首先通过链轮的安装孔安装一个螺母和螺栓。然后，使用 G 形夹将钻头安装到~~餐桌~~工作台上，并将链轮安装到卡盘上。一旦安装牢固，拉链可以用在钻机的触发器上，使其以最大速度运行。这样你就可以腾出两只手来操作角向磨光机了。当链轮毛坯在钻头中旋转时，使用磨盘小心地磨掉链轮毛坯的表面。

尽管这种设置有偷工减料的性质，但它允许我很容易地将链轮加工到合适的宽度。我甚至能够整齐地使齿变尖，这有助于链条在轻微错位时运行得更好。

## 修整牙齿

![](img/51282baead8d54d7cd4e500d29e57e44.png)

The teeth are quite ragged after the initial rough cut with the angle grinder. It’s necessary to refine them further.

在这一点上，你应该有一个整洁加工链轮空白丑陋，矮胖的牙齿。虽然我的父亲在我之前已经完成了这项任务，但是角磨机实在是太粗糙了，无法完成切齿。相反，使用旋转工具。我已经成功使用了 [953 磨石](https://www.dremel.com/en_US/products/-/show-product/accessories/953-1-4-aluminum-oxide-grinding-stones)，然而 [9903 切割头](https://www.dremel.com/en_US/site-search-results?blogsearch=9903+)是切割钢材的更好选择。这使得人们可以缓慢而小心地加工牙齿，而不会有意外地完全切掉牙齿的风险。

在所有这些切割之后，你可能会发现你的模板不再贴在链轮上。使用现有链轮作为视觉参考，小心地打磨轮齿。围绕链轮工作，一点一点地加工，同时反复缠绕链条以检查配合。链条需要能够平滑地与链轮啮合，并且容易滑上滑下，以避免卡滞或脱轨。实现这一点的诀窍是为滚子制作一个漂亮的圆形凹槽，同时确保齿具有光滑的轮廓，不会在链条滑动时卡住链条。与现有链轮进行比较是了解您想要的几何形状的一个好方法。

![](img/cf6d4f22a18d199bf8b6528f48132c07.png)

Cutting the teeth involves careful machining followed by checking the mesh with a test piece of chain. This continues around the sprocket, using trial and error to get a workable profile on each tooth.

在这个过程中，我不得不把很多金属从链轮上去掉，结果牙齿看起来很粗糙。他们中的一些看起来非常薄和尖，其他的看起来像微小的小块。这与你在教科书上看到的理想链条轮廓相差甚远。然而，我在这种类型的其他构建上的经验让我相信这是可行的。大约一个小时后，我让我的链轮齿与测试链啮合良好，并着手将其安装到踏板车上。

## 证据就在拍摄中

![](img/5c5a34460705a3b2f728601a81f485fa.png)

The sprocket under test. The right image shows the chain skipping. The tensioner helps keep the chain on the sprockets during these events.

如果你已经走了这么远，恭喜你！你已经有了一个 DIY 链轮，可能看起来有点时髦，但希望啮合良好，并准备测试。把它装起来，明智地润滑，尽情享受吧！

我急于测试我的创作，并开始工作。像往常一样，安装链轮需要一点时间。安装孔一开始不合适，所以我用一个现有的链轮作为模板，用碳化钨钻头再加工出一点东西。链条也需要延长以适应更大的小齿轮。

在去兜风之前，我支起了踏板车，并测试了传动系统。我加快了马达的转速，链条果然带动了后轮。谢天谢地，链条没有脱轨或卡在新链轮上，所以事情看起来很好。有一些小的跳跃，但我不太担心。一个 500 W 的马达，一个 80kg 的骑手，以及由低碳钢制成的新链轮，我相当有信心它会磨损得很好，随着时间的推移变得更平滑。由于链条状况不佳，我用手头仅有的东西——75W 差速器油，给它上了大量润滑油。它很臭，但它是一种很好的链条润滑剂。

![](img/4f43fe7207b19d99cbe5f122abf37aae.png)

I was out front, right up until the battery ran out.

令我非常高兴的是，新的链轮表现得像做梦一样。无论是在重载下加速还是以最高速度飞行，链条只会随着我的骑行变得更加平稳。在街区跑了几圈后，我给自己的电池充好电，开始了极速奔跑。沿着一条笔直的道路，我设法达到了 41 公里/小时，刚好超过了我的目标。简单地说，我欣喜若狂。

我现在已经在链轮上增加了许多英里，它继续保持良好。虽然它可能不像商业制造的零件那样坚硬，但它是无法获得的一个很好的替代品。我的滑板车现在跑得相当快了，多亏了一点 DIY，我能够在直线拖曳中击败我所有的朋友。我称之为成功的构建！

 [https://www.youtube.com/embed/hIPoUW3z_ZU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hIPoUW3z_ZU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

