# 关于 HMDs 中的 FOV，你可能不知道的一切

> 原文：<https://hackaday.com/2019/06/21/everything-you-probably-didnt-know-about-fov-in-hmds/>

虚拟现实头戴设备几年来一直在寻找新的生命，当谈到头戴显示器时，视野(FOV)是每个人都渴望发现的规格之一。Valve Software 发布了一份高度技术化但易于理解的[文档，解释了为什么视野(FOV)在涉及头戴式显示器时是一件复杂的事情](https://www.valvesoftware.com/en/index/deep-dive/fov)。当涉及到相机之类的东西时，FOV 相对简单，但当涉及到使用镜头将图像放在眼球旁边时，它变得复杂得多，很难定义或容易测量。

![](img/0761bea0624406497da8d5b5ad723ded.png)

模拟 FOV 如何受到眼部缓解的影响【来源: [Valve 软件](https://www.valvesoftware.com/en/index/deep-dive/fov)】

该文档详细介绍了头戴式显示器的一些有用细节，设计权衡，并自然地特别谈到了全新的 Valve Index VR 头戴式设备。该指数使用专有镜头结合轻微向外倾斜的每只眼睛的显示器，它们精确地解释了每个设计点获得的好处。眼睛间距(眼睛到镜片的距离)、镜片形状和安装(限制眼睛的实际距离)以及可调节性(因为脸和眼睛的形状不同)都有作用。这是一个每一毫米都很重要的情况。

如果说 Valve 试图在这篇文章中提出一个要点，那就是“很难用一个数字来有效地描述 HMD 的视野。”他们计划发布更多关于调制和光学主题的信息，所以请留意他们的[阀门指数深潜发布列表](https://www.valvesoftware.com/en/index/deep-dive/)。

从黑客的角度来看，Valve 的 VR 努力仍然很有趣，作为一个组织，他们似乎对能够修改和扩展他们的产品非常感兴趣。Vive 追踪器是独立的，有一个可访问的硬件引脚,目的是让黑客攻击更容易。我们还[看了看 Valve 的 AR 和 VR 原型](https://hackaday.com/2016/06/22/behold-valves-vr-and-ar-prototypes/)，这让我们对他们如何以及为什么选择他们所做的方向有了一些了解。