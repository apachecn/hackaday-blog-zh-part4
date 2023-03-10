# 哈利·波特魔杖破解让魔法成真

> 原文：<https://hackaday.com/2020/04/05/harry-potter-wand-hack-makes-magic-real/>

一位智者曾经观察到，任何足够先进的黑客技术都和魔法没什么区别。这是真的，当你以正确的方式挥动哈利波特魔杖时，这个来自 Jasmeet Singh 的酷建筑会神奇地打开一个盒子。是魔法吗？不，这是一个巧妙的黑客技术，它使用计算机视觉来跟踪魔杖，并识别你何时做出魔法手势。

这个技巧是基于环球电影公司在他们的哈利波特主题公园中使用的相同技术，正如一项名为“[用于跟踪被动魔杖并根据检测到的魔杖路径激活效果的系统和方法](https://patents.google.com/patent/US20140240102A1/en)”的专利中所详述的。基本的想法是在棒的末端有一个反光点，反射来自摄像机周围的一组红外发光二极管的光。一台红外敏感相机将这种反射光检测为亮点。这种摄像机被连接到一个计算机视觉系统中，该系统跟踪圆点的路径，如果它遵循某个模式，就会触发动作。

[Jasmeet]构建的版本使用了 Raspberry Pi NoIR 相机和运行 OpenCV 的 Raspberry Pi 3。这将输入到检测字母表字母的机器学习图中。如果检测到的字母是 A(阿洛玛霍拉，哈利波特的打开咒语)，那么盒子就会打开。如果是 C，盒子就关上了。这些都是使用 Python 绑定在一起的。

这是一个整洁的建筑，结合了许多有趣的技术，可以让孩子们开心一会儿。您还可以进一步扩展它，比如添加一条死亡射线，如果您跟踪 Sectumsempra 的 S，就会触发这条射线。这会教他们不要乱用黑魔法。

 [https://www.youtube.com/embed/9DyAehKEF4Q?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent](https://www.youtube.com/embed/9DyAehKEF4Q?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent)



 [https://www.youtube.com/embed/9DyAehKEF4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9DyAehKEF4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

