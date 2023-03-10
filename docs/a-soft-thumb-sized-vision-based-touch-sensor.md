# 一个柔软的拇指大小的视觉触摸传感器

> 原文：<https://hackaday.com/2022/03/12/a-soft-thumb-sized-vision-based-touch-sensor/>

德国马克斯·普朗克智能系统研究所的一个团队开发了一种[新型拇指形状的触摸传感器](https://www.nature.com/articles/s42256-021-00439-3)，能够在结构的整个表面上解析接触的力度及其方向。该系统旨在用于灵巧的操纵系统，由容易获得的组件构成，因此应该在不破坏银行的情况下扩大到更大的组件。第一步是在坚硬的金属骨架上放置柔软的外壳，然后使用结构光技术对其内部进行照明。由此，通过观察内部包络如何扭曲结构化照明，机器学习可以用于估计整个表面上与皮肤接触的剪切力和法向力分量。

这里的新奇之处在于他们将[光度立体处理](http://www.ihaveaurl.com/vgrg/Woodham80.pdf)与其他[结构光](https://opg.optica.org/aop/fulltext.cfm?uri=aop-3-2-128&id=211561)技术相结合，仅使用一台相机。相机图像被直接馈送到预先训练的机器学习系统(遗憾的是，关于系统的这一部分的细节有点缺乏)，该系统直接输出接触形状和力分布的估计，据报道空间精度好于 1 mm，力分辨率低至 30 毫牛顿。通过直接估计法向力和剪切力分量，接触的方向可以分解到 5 度。该系统非常敏感，据报道，它可以通过观察自身重量引起的皮肤变形来检测自己的姿势！

我们还没有涵盖所有的光学传感项目，但这里有一个使用[线性 CIS 传感器将任何电视变成触摸屏](https://hackaday.io/project/27155-magic-frame-turn-everything-into-a-touch-area)。当我们谈论使用相机作为传感器时，这里有一个使用[光纤读取多个光门](https://hackaday.com/2019/08/30/fibergrid-an-inexpensive-optical-sensor-framework/)的简单方法，只需一个相机和 OpenCV。

 [https://www.youtube.com/embed/lTAJwcZopAA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lTAJwcZopAA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示！