# 还有！XOR 的 DEF CON 29 电子徽章是一个组装拼图

> 原文：<https://hackaday.com/2021/08/02/andxors-def-con-29-electronic-badge-is-an-assembly-puzzle/>

多年来，我一直期待着看到#Badgelife 发电站推出的每个新的非官方硬件徽章，即和！异或。新的有趣的组件，虚拟现实游戏和迷因的混合，你永远不知道他们会扔出什么。

周四，一个装着最新产品的泡泡包放在了我的桌子上， [the AND！专为 DEF CON 29](https://hackaday.io/project/180738-andxor-dc29-badge) 打造的 XOR 电子徽章，本周末以现场和在线会议的形式举行。虽然前几年都加大了复杂性和制造魔术的赌注，但考虑到全球疫情和全球芯片短缺的不确定性，他们采取不同的策略也就不足为奇了。我们这里有一个徽章黑客难题，挑战你只是想出如何把事情放在一起！

## 硬件

 [![ANDnotXOR_DC29_meme-packaging](img/3050b3649e129896994a31031c3a8592.png "ANDnotXOR_DC29_meme-packaging")](https://hackaday.com/2021/08/02/andxors-def-con-29-electronic-badge-is-an-assembly-puzzle/andnotxor_dc29_meme-packaging/)  [![ANDnotXOR_DC29_whats-inside](img/0ff9a99c85558fb72f2685c8dd5c589b.png "ANDnotXOR_DC29_whats-inside")](https://hackaday.com/2021/08/02/andxors-def-con-29-electronic-badge-is-an-assembly-puzzle/andnotxor_dc29_whats-inside/) 

拆开徽章，很明显这是一个焊接套件。除了主 PCB 和四个子 PCB 之外，还有一个用胶带包裹的小拉链包，以及两个硬币电池、一个电池座和一个漂亮的彩色挂绳。你必须把所有这些东西放在一个包裹里才能运输，所以 meme 工厂决定推出一包“Damonitos”，这是一个关于 Doritos 品牌玉米片的游戏，也是 badge collective 最近采用的标签吉祥物 Matt Damon。我没有问为什么，你也不应该问。

问题是，这里没有可编程的东西；这是一个硬件徽章。稍后我将深入探讨组装细节，但这看起来像是表面贴装电阻、电容和晶体管，以及一个通孔调整端口。这是一个聪明的方法来回避 2021 年可靠地采购任何数量的微控制器的问题。

[![](img/f5a9531ba6a8b52e2f20962393318f3d.png)](https://hackaday.com/2021/08/02/andxors-def-con-29-electronic-badge-is-an-assembly-puzzle/andnotxor_dc29_badge-front/)[![](img/d9dc778eed58f7d7fedf7d4f063625ff.png)](https://hackaday.com/2021/08/02/andxors-def-con-29-electronic-badge-is-an-assembly-puzzle/andnotxor_dc29_badge-rear/)

板子本身明显就是奥什公园的“天黑后”待遇(果然，他们的 logo 就在板子背面)。标志性的处理使用黑色基板(电路板本身)，透明阻焊膜让铜迹线透过，ENIG 电镀金色焊盘，以及白色阻焊膜。

## 组装拼图

[![](img/34a356a4efa1399a6a45a5b5f58a57f1.png)](https://hackaday.com/wp-content/uploads/2021/07/ANDnotXOR_DC29_component-glyphs.jpg) 我想和！XOR 在记录他们的徽章(T4)方面无疑是最好的，但是在他们设计的谜题范围内。在这种情况下，大多数人会拿起原理图，开始在电路板上粘贴进行组装。但是到他们的项目页面，你会发现没有这样的资源。

你会发现[鼓励打破用作元件参考的字形密码](https://hackaday.io/project/180738/log/195788-the-cipher)紧挨着电路板背面的每个足迹。密钥中使用了 16 个图标，对于十六进制值来说这是个不错的数字，但我只是随便说说。我还没有时间开始这项挑战，但这是我现在想做的事情。对我完成实际工作的前景并不乐观， *thaaaaaanks* 还有！异或。

三条腿的足迹很容易找到，但两种不同的晶体管胶带让我想到你需要建立 PNP 和 NPN。即使你解决了这个问题，破解了电阻值的密码，还有一个路由难题。

[![](img/41669e772aebba3291dac582e8c65d82.png)](https://hackaday.com/2021/08/02/andxors-def-con-29-electronic-badge-is-an-assembly-puzzle/andnotxor_dc29_pbc-faces/)[![](img/6f0e22ee0f9b193494d161c3ce6e1c85.png)](https://hackaday.com/2021/08/02/andxors-def-con-29-electronic-badge-is-an-assembly-puzzle/andnotxor_dc29_pcb-traces/)

子 PCB 本身是挑战中有趣的一部分。每个的正面都有两个面，在边缘分成两半。顶部和底部的齿形边缘与主 PCB 正面的尺寸相匹配。出于某种原因，这使人想起吃角子老虎机，在那里你希望每一次旋转都像图像一样匹配。在子板的背面，您可以看到它们每个都以电气方式将走线引向不同的目的地。

我被告知，这块板的大小与疾控中心官方的 COVID 疫苗卡完全匹配(我想这也解释了它附带的酒精擦拭布和创可贴)。其他值得注意的功能包括“圆形”边缘，使用 20 世纪 80 年代风格的 8 位圆角。徽章挂绳的方孔延续了美感。

虽然这并没有上升到像[他们的 DC27 徽章](https://hackaday.com/2019/07/29/hands-on-andxor-def-con-27-badge-ditches-bender-adopts-light-pipes/)那样的高度，其中包括与 PCB 集成的磷光贴纸，用于空间效果的光管，以及点画丝网的巧妙使用，但我们生活在一个与两年前非常不同的世界。在我们的生活发生天翻地覆的变化后，令人耳目一新的是，与前几年的多人游戏、仅在骗局中挑战相比，你的普通人更容易接受新的挑战。即使你手中没有这个工具包，你也应该能够拍摄我在本文中包括的图像，绘制迹线，并破解代码来找出电路。我被迷住了。

还有！XOR 整合了 800 个徽章套件。到目前为止，大约有 400 台通过他们的网上商店售出。其余的将在 DEF CON 29 上亲自分发，他们将再次恢复在全球各地进行“本地投放”的做法。如果你想得到一个，并且能够容忍——甚至拥抱——持续不断的迷因流，在接下来的几天里[关注他们的社交](https://twitter.com/ANDnXOR)。