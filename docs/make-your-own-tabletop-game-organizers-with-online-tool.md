# 用在线工具制作你自己桌面游戏组织者

> 原文：<https://hackaday.com/2022/02/19/make-your-own-tabletop-game-organizers-with-online-tool/>

围绕销售配件建立了一个充满活力的家庭手工业，以改善桌面游戏的存储和组织，但更有 DIY 意识的人肯定会喜欢[【Steve Genoud】的 deckinabox 工具](https://deckinabox.sgenoud.com/)，它可以创建 3D 打印设计，或更适合折叠纸或卡片纸的设计。制作自己的组织者既经济又令人满意，[Steve]的工具旨在使定制变得简单易行。

[![](img/5705e72ab83d1296320e43b93e6b2a50.png)](https://hackaday.com/wp-content/uploads/2022/02/deckinabox-token-tray.jpg)

The tool can also generate models for folded paper or cardstock.

例如，用于定制 3D 可打印令牌托盘的界面从简单的圆角容器开始，可以通过添加水平或垂直分隔符将该容器分割成附加区域。默认情况下是将一个给定的区域从中间分开，但是当然可以指定每个维度。像边缘的圆角(为了更容易的令牌舀)和其他细节都是自动处理的。每次更改后，一个方便的 3D 视图都会实时呈现设计。

[Steve]发表了一篇博客文章，详细介绍了该工具是如何制作的，并大量使用了[的 replicad](https://github.com/sgenoud/replicad)，[Steve]自己的库来生成基于浏览器的 3D 模型代码。对以编程方式生成 3D 模型的想法感兴趣，并想用它来制作自己的模型？别忘了也来看看[OpenSCAD](https://hackaday.com/2021/04/17/guide-to-mastering-openscad-costs-roughly-the-same-as-openscad/)；很可能它比人们想象的更容易使用，功能也更强大。