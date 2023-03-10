# DIY 激光散斑成像揭开隐藏的细节

> 原文：<https://hackaday.com/2021/09/17/diy-laser-speckle-imaging-uncovers-hidden-details/>

这听起来确实像是“激光散斑成像”是那种你需要拨款进行实验的东西，[但是正如【anfractuosity】最近展示的那样](https://www.anfractuosity.com/projects/fun-with-speckle-patterns/)，你可以通过相对简单的硬件设置和一些常见的开源软件包获得一些非常令人印象深刻的结果。事实上，你可能已经拥有了在你自己的车间里完成这项工作所需的所有组件，只是你不知道而已。

任何玩过激光笔的人都熟悉光束照射在某些物体上时观察到的闪光效应。这就是激光散斑，它是由光束反射表面纹理的微观变化并产生光学干涉而产生的。虽然这种现象在很大程度上阻止了激光束成为有效的直接照明源，但它可以用作一种方法来测量看似平坦的表面中极其微小的扰动。

[![](img/72a367fb970cf83dd4ad06d93ae99664.png)](https://hackaday.com/wp-content/uploads/2021/09/laserspeckle_feat.jpg)

在这个演示中，[anfracturity]将一个简单的红色激光指示器与显微镜的 25 倍物镜结合起来，产生了一个更宽、强度更低的光束。当这种漫射光束投射到墙上时，可以清楚地看到表面纹理产生的散斑图案。对于肉眼来说*不*明显的是，用手触摸墙壁实际上会产生散斑图案的变化。但是如果你在拍摄前后拍摄高分辨率的照片，这些照片可以通过 OpenCV 来突出差异，并显示出幽灵般的手印。

然后在计算器上按下一些按钮之前和之后，使用相同的技术。最终清理后的图像不仅清楚地显示了显示屏上的数字，还突出显示了被触摸的各个按钮。看到这个例子，不难想象这种技术会有一些邪恶的应用。攻击者可以使用激光散斑成像来确定锁定键盘或报警面板上的哪个按钮被按下了吗？

 [![laserspeckle_detail4](img/f70b9c3f6ebf65540a54ec20d1df71e2.png "laserspeckle_detail4")](https://hackaday.com/2021/09/17/diy-laser-speckle-imaging-uncovers-hidden-details/laserspeckle_detail4/)  [![laserspeckle_detail6](img/12955258023b7979aa83a5acb1111413.png "laserspeckle_detail6")](https://hackaday.com/2021/09/17/diy-laser-speckle-imaging-uncovers-hidden-details/laserspeckle_detail6/) 

幸运的是，听起来将这样的攻击付诸实践是相当困难的。首先，在拍摄前后照片时，相机和激光器需要处于完全相同的位置，这对于秘密行动来说几乎是不可能的。其次，正如下面的视频所证明的那样，印记往往会很快腐烂。事后拍摄必须在键盘被触摸的几分钟内进行，这使得在野外拍摄更加困难。

目前还不清楚这项技术在黑客和创造者群体中会有什么实际应用，[所以我们很想听听你可能想到的任何东西。无论如何，这是一个令人印象深刻的成就，也是现代爱好者的一个很好的例子。](https://hackaday.com/submit-a-tip/)

 [https://www.youtube.com/embed/fbOuCrMG_F8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fbOuCrMG_F8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

