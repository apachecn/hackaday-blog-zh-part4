# PCB 艺术家之路:如何制作真正漂亮的电路板

> 原文：<https://hackaday.com/2020/01/13/the-way-of-the-pcb-artist-how-to-make-truly-beautiful-circuit-boards/>

对于硬件黑客来说，制作自己的 PCB 是必经之路。通常，这是一个值得骄傲的时刻，我们中的许多人选择通过在屏幕上自我夸大的功劳，或者一个笑话或个人标志来永垂不朽。然而，就艺术定制的 PCB 而言，天空真的是极限，这是[TwinkleTwinkie]，[的专长，他的 Supercon talk 涵盖了在传统 PCB 工艺边缘工作时可能遇到的一些陷阱。](https://www.youtube.com/watch?v=5G-uHDRKI1k)

[TwinkleTwinkie]的作品通常是这样或那样的徽章——它们应该挂在你脖子上的挂绳上，作为一个别针，或者作为一个装饰添加到另一个徽章上。最重要的是美观，风格和功能一样重要。他的徽章有各种各样的灵感，如 *Futurama、* *Alice in Wonderland* 和 GIF 社区的恶作剧，他的徽章将明亮的彩色板与大量的 led 和艺术丝网印刷融合在一起，创造出电子艺术作品

## 防止 PCB 工厂破坏艺术品

如今，PCB 工厂在丝网印刷、阻焊颜色和其他选项方面提供了比以往更多的选择。然而，从根本上说，他们主要关心的是生产可靠、精确、电子功能板——这可能会给#badgelife 黑客出于更美观的原因进行设计带来问题。

![](img/aede3df1b5161d8efe96887d7059bea9.png)

On the left, a prototype, and on the right, a model with the black silkscreen part, showing how the LEDs appear dimmer.

[TwinkleTwinkie]在开发[电弧徽章](https://hackaday.io/project/165320-arc-badge-dc27-indie-badge)的过程中遇到了这个问题，这是一个旨在复制*钢铁侠*和*复仇者联盟*电影中著名的电弧反应器的作品。徽章的基本想法是有一个承载所有硬件的基础 PCB，以及一个垫片，然后第三个顶层由一个 PCB 组成，led 将通过它发光。原型板工作良好，fab house 在 1.6 毫米厚的 FR4 上生产，带有白色丝网印刷和红色阻焊膜。对于最终产品，想要一个稍微花哨一点的东西，黑色丝网被选中。通过 PCBWay 订购，这就需要使用他们的“高级生产工厂”,以及更长的交付时间，但几周后电路板就准备好了。

![](img/8e6a585f7e9867fee768c3993baaa9e9.png)

A comparison with the final, fixed part on the left and the black silkscreen part on the right. The final design allows much more light to pass through.

不幸的是，尽管黑色丝网印刷与红色阻焊膜形成鲜明对比，看起来很棒，但还是有一个问题。当[TwinkleTwinkie]要求黑色阻焊膜时，这也导致了 FR4 材料的变化，变成比原型板更不透明的不同等级。这导致 led 显示非常暗淡，破坏了 ArcBadge 所需的视觉效果。变暗是如此重要，以至于用户在 t 恤下佩戴徽章时将不再有发光效果。它需要与原型进行比较才能弄清楚发生了什么。PCBWay 在改用黑色丝网印刷时，只是使用了更高级的材料。鉴于 PCB 是作为电子产品出售的，而不是因为它们的光学质量，它们本身没有做错任何事情——但不管怎样，新电路板不适合这个目的。

## 点，点，再点

解决方案很简单——电路板需要重新排序。为了保证发光二极管能够发出耀眼的光芒，我们采取了预防措施。最终的电路板切换回白色丝网印刷。作为额外的预防措施，如果 PCBWay 继续使用新材料，新部件的厚度为 0.8 毫米，使其阻挡的光线更少。

重新设计后,[TwinkleTwinkie]有 250 个杯垫可以分发，但他为顾客提供优质产品的承诺值得称赞。尽管没有人直接犯错，但如果没有重新设计，最终的产品会有点令人失望。交付时，Arc 徽章会散发出最佳的光芒，我们相信每个参与其中的人都会因为这次经历而变得更加明智！

 [https://www.youtube.com/embed/5G-uHDRKI1k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5G-uHDRKI1k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

