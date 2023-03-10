# 自动绕线机只需简单的硬件和软件就能完成

> 原文：<https://hackaday.com/2021/07/25/automatic-coil-winder-gets-it-done-with-simple-hardware-and-software/>

我们越来越期待看到机电一体化项目包含一个标准的组件，如步进电机，Arduinos，丝杠，同步带和滑轮，以及铝型材。因此，当一个项目打破了这种模式，哪怕只是一点点，我们都会注意到。

与这种硬件黑客通用语有些不同的是[tuenhidy]的[自动绕线机](https://www.instructables.com/GRBL-Based-Coil-Winder-From-Water-Pipe/)，它使用简单的 PVC 管和配件作为框架，而不是铝型材和 3D 打印的连接器。便宜，容易获得，容易加工，PVC 在这里做得很好，可能会在任何力度低和精度不重要的项目中使用。PVC 框架装有两个驱动电机，一个用于将电线缠绕在模板上，另一个用于驱动丝杠来回移动模板。带有 CNC 保护罩的 Arduino 负责驱动电机，这样做所需的 g 代码是由一个简单的电子表格生成的，该表格考虑了所需的匝数、层数、线轴的尺寸和电线的直径。下面的视频展示了这台机器的测试过程，结果非常整洁。

作为一个如此乏味的任务，这远远不是我们看到的第一个线圈绕线机。有些[坚持标准的设计语言](https://hackaday.com/2021/03/24/coil-winding-machine-makes-it-easy/)，有些[完全朝着另一个方向发展](https://hackaday.com/2020/11/16/automatic-winder-takes-the-drudgery-out-of-tesla-coil-builds/)，但是它们都很有教育意义，看起来很有趣。

 [https://www.youtube.com/embed/dLUy6qs0csU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dLUy6qs0csU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

