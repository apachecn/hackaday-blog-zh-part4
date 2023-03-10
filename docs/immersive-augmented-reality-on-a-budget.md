# 预算有限的沉浸式增强现实

> 原文：<https://hackaday.com/2019/02/18/immersive-augmented-reality-on-a-budget/>

到目前为止，我们都已经看到了廉价的耳机，它们本质上是将智能手机贴在离你的脸几英寸远的地方，作为 Oculus Rift 等设备的低成本替代品。价格低至几美元，在预算有限的情况下，很难击败这些虚拟现实实验设备。但是，如果您对增强现实更感兴趣呢？在增强现实中，渲染的图像叠加在您的真实世界视图上，而不是取代它。

[![](img/af2e560edfd1d01af0fdc131e65a58af.png)](https://hackaday.com/wp-content/uploads/2019/02/arheadset_detail.jpg) 事实证明，现在有廉价的耳机也可以和你的手机一起使用。[【kvtoet】在全球速卖通](https://hackaday.io/project/163805-less-than-100-high-fov-mobile-ar-glasses)花了 30 美元买了一个这样的小玩意，并把它作为一个比耳机本身更有能力的增强现实体验的基础。该项目还处于早期阶段，但到目前为止，这种简单的耳机和一些从廉价的中国智能手机中解放出来的硬件的结合，似乎有望为任何希望进入这一迷人领域的人提供一个低于 100 美元的开发平台。

这些廉价的增强现实耳机本身只是在镜片内部显示智能手机屏幕的反射。通过特别设计的应用程序，这种效果可以用来给佩戴者一种印象，即手机屏幕上显示的对象实际上在他们的视野中。可以肯定的是，这是一个很好的效果，但是在实际应用中并没有太大的作用。为了将这变成一个有用的系统，手机需要能够看到佩戴者所看到的东西。

为此，[kvtoet]将 VKWorld S8 智能手机的摄像头模块重新安置在耳机的正面。除了相对较高的成本，这款手机被选中是因为它有一根长长的摄像头带状电缆。由于摄像头位于耳机外部，因此创建了一个 Android 应用程序，该应用程序会定期闪烁明亮的 LED，并在摄像头的反馈中寻找反射。这些反射然后被用来定位现实世界中的物体和标记。

在休息之后的视频中，[kvtoet]演示了如何使用这种技术。这款手机能够足够快速准确地跟踪躺在沙发上的反光镜，从而可以用来实时调整虚拟物体的渲染。随着耳机的移动，它给人的感觉是佩戴者实际上是从不同的角度和距离观看一个真实的物体。这样一个简单的系统，效果并不完美，但令人兴奋的是，现在这种技术正在落入修补者的预算中。

如果你不想走 DIY 路线，Leap Motion 已经[推出了一款开源增强现实耳机](https://hackaday.com/2018/04/10/leap-motion-announces-open-source-augmented-reality-headset/)，这让我们非常兴奋。[我们仍在等待硬件](https://hackaday.com/2019/02/03/leap-motions-project-north-star-gets-hardware/)，但这并没有阻止来自[的黑客们同时推出一些迷人的增强现实应用](https://hackaday.com/2019/01/09/smartphone-app-uses-ar-to-visualize-the-rf-spectrum/)。

 [https://www.youtube.com/embed/u75PpZSYU68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u75PpZSYU68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

