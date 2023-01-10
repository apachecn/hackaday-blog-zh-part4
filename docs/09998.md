# 麻省理工学院的刷毛机器人解开机器人难题

> 原文：<https://hackaday.com/2021/05/08/mits-new-robot-brushes-your-hair/>

不管你愿不愿意承认，头发对自我形象来说很重要，不能自己处理头发会让人感觉失去了独立性。为了帮助行动不便的人，[麻省理工学院 CSAIL 的研究人员创造了一个梳头机器人](https://docs.google.com/document/d/1SSXM6mOiI9GCISY0Io_1k7NE6nmBmm4z0Nl90YzETCM/edit?usp=sharing)，它结合了一个带有力反馈和闭环控制的摄像头，可以在飞行中调整任何头发类型，从直发到卷发。他们通过将头发视为柔软纤维的双螺旋来实现这一点，并开发了一种数学模型来解开它们，就像人类一样——通过从下往上的工作。

[![](img/686d270125a3e3b2594f32f56aea58c7.png)](https://hackaday.com/wp-content/uploads/2021/04/hair-types.jpeg) 它可能看起来像绑在机器人手臂上的发刷，但它远不止如此。在它开始刷牙之前，机器人的摄像头会拍摄一张照片，并将其裁剪成一个纯毛发数据的矩形。这个图像被转换成灰度，然后程序分析 x/y 图像梯度。头发越直，它在 x 方向上的边就越多，而卷发的分布就越均匀。最后，程序计算直度与弯曲度的比值，并用这个数值来设定疼痛阈值。

这种刷子装备有传感器，可以测量被刷时施加在头发和头皮上的力，并将这种输入与用它来刷自己头发的人建立的基线进行比较。我们认为，如果机器人可以先抓住头发的一部分，这样人就不会感觉到对头皮的拉力，并在从头皮向下刷之前先刷完发尾，这将是一件很棒的事情，但我们承认这要求太高了。也许他们可以让它对“嗷”和“哎哟”这样的感叹词做出反应。人体试验仍在进行中。现在，看它在休息后轻轻地刷出各种假发。

即使我们有一头容易缠结的卷发，我们也可能会让这个机器人为我们梳头。[但是这个理发机器人？](https://hackaday.com/2020/07/14/a-robotic-stylist-for-your-lockdown-lengthened-locks/)我们没那么勇敢。

 [https://www.youtube.com/embed/3dHCdQBagfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3dHCdQBagfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

