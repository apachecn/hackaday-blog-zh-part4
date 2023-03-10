# 发布 Python 包的备忘单

> 原文：<https://hackaday.com/2018/12/13/a-cheat-sheet-for-publishing-python-packages/>

[Brendan Herger]被警告发布 Python 包的过程将会很有挑战性。然而，他喜欢挑战，所以他兴致勃勃地去迎接挑战。这个令人疲惫的过程让他分享了一个发布 Python 包的[备忘单，目的是让下一次更顺利，同时也让其他人从他的经验中受益，并有一个良好的开端。](https://www.hergertarian.com/cheat-sheet-publishing-a-python-package)

[Brendan]将发布 Python 包描述为“通过脆弱的交换将许多不同的解决方案捆绑在一起。”他的备忘单采用有序工作流的形式，将一切都安排妥当，并预先做出一些关于格式化和持续集成(CI)的重要决定和建议。

这个指南很简短，但是[Brendan]犯了一些错误，走进了死胡同，希望其他人不会犯同样的错误。整个事情来自于他在深度学习方面的工作，以及他创建一个包的愿望，这个包允许快速构建和迭代深度学习模型。

深度学习是一种机器学习，涉及在大量数据中寻找表示。[Brendan]在一个项目中使用它来[自动决定 Reddit 帖子是否包含《星球大战》情节剧透](https://github.com/bjherger/spoilers_model)，我们最近看到它以一种方法为特色，[只在蜂鸟出现的情况下捕捉视频镜头](https://hackaday.com/2018/08/31/hummingbirds-3d-printing-and-deep-learning/)。