# 激光透过钥匙孔看到

> 原文：<https://hackaday.com/2021/12/21/laser-sees-through-keyhole/>

斯坦福的那些家伙一定看了很多詹姆斯·邦德的电影。他们的最新发明是一种可以通过钥匙孔对整个房间成像的激光。我们认为这将很快出现在一些间谍电影中。可以[看代码](https://github.com/computational-imaging/KeyholeImaging)或者看下面的视频。

这项技术被称为 NLOS 或非视线成像。以前的方法需要扫描大面积来寻找隐藏物体的间接光。这种新方法使用激光来寻找移动的物体。基于运动和算法的间接数据变化可以逆转测量结果以确定物体的特征。

如果你担心邻居偷窥狂，你可以放松了。恢复的图像令人惊叹，但质量不是特别高。尽管如此，考虑到它们是间接制作的，它们很棒，但是你不会制作出精细的细节。

如你所料，这项工作计算量很大。GitHub 仓库有 Python 代码和数据，如果你不想建立自己的激光设置，你可以使用。如果你有一个有足够内存的 GPU，你可以使用 CUDA 来加速计算。

NLOS 成像并不是什么新鲜事，但仍有新的方法等待被发现。我们喜欢激光的新用途。我们已经见过[激光逻辑门](https://hackaday.com/2021/01/16/interference-patterns-harnessed-for-optical-logic-gates/)。我们还是想试试[的激光烤箱](https://hackaday.com/2021/09/28/microwave-ovens-need-more-power-use-lasers-instead/)。

 [https://www.youtube.com/embed/Veo27qhrI20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1&wmode=transparent](https://www.youtube.com/embed/Veo27qhrI20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1&wmode=transparent)

