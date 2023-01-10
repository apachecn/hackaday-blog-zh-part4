# 用 F-K 偏移寻找拐角

> 原文：<https://hackaday.com/2019/08/22/looking-around-corners-with-f-k-migration/>

非视线(NLOS)成像背后的概念似乎很容易理解:激光从一个表面反射光子，照亮该表面视线内的物体，但不照亮成像设备。然后被隐藏物体反射或折射的光子返回到激光的位置，在那里它们被捕获并处理以形成图像。本质上，这允许一个人使用任何表面作为镜子来观察角落。

这种方法的主要缺点是分辨率低并且对噪声非常敏感。这使得斯坦福大学的一个团队尝试用各种方法来提高 T1。正如*科技简报* [对研究生【大卫·林戴尔】](https://www.techbriefs.com/component/content/article/tb/stories/blog/34990)的采访中所详述的，一项重大改进来自一种超快速快门解决方案，它阻挡了从被照亮的墙壁返回的大部分光子，防止被物体反射的光子被这种噪声淹没。

获得所需成像质量的关键是这种 f-k 偏移算法，包括有光泽和难以成像的物体。正如休息后嵌入的视频中所解释的，他们看了看地震学领域中使用的方法，其中振动用于对地壳内部进行成像，以及合成孔径雷达等。产生的算法使用一系列傅立叶变换、频谱重采样和插值以及傅立叶逆变换来将接收到的数据处理成可用的图像。

这不是一个新话题；我们早在 2011 年就报道过这个[的一个简单实现，以及 2015 年英国研究人员](https://hackaday.com/2011/04/18/laser-camera-sees-around-corners/)的一个[项目。这项新研究显示了明显的改进，使这种技术在实际应用中更加可行。](https://hackaday.com/2015/12/14/seeing-around-corners-with-frickin-lasers/)

研究人员指出，这种技术的明显应用包括激光雷达数据处理和自动驾驶汽车等。更具挑战性的是像医学成像这样的东西，人们甚至可以对通常被组织或骨骼隐藏的东西进行成像。

对于那些有兴趣了解更多信息的人来说，SIGGRAPH 2019 [上展示的论文、数据集和更多信息可在此处](http://www.computationalimaging.org/publications/nlos-fk/)获得。

 [https://www.youtube.com/embed/BVYfzLXUi48?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BVYfzLXUi48?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

