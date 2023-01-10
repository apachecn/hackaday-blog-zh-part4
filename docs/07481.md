# 使用这些 OpenSCAD 助手快速 3D 打印翼型

> 原文：<https://hackaday.com/2020/08/14/quick-3d-printed-airfoils-with-these-openscad-helpers/>

你知道这是怎么回事。你正在做一个项目，需要移动空气或水，或者移动*通过*空气或水，但是你的 3D 设计印章和/或你的空气动力学知识阻止你做正确的事情？如果你使用 OpenSCAD，你就没有理由制造不必要的湍流:只需点击你最喜欢的箔片，然后把它粘贴进去。【本杰明】的[基于网络的实用程序](http://chaaawa.com/airfoils/index.cgi?o=name&n=50&p=2)已经搜集了神奇的 [UIUC 翼型数据库](https://m-selig.ae.illinois.edu/ads/coord_database.html)并为你做了艰苦的工作。

虽然他最初写这个实用程序是为了给铸造厂制造鼓风机叶片，但他也计划尝试一些 3D 打印的风力涡轮机，自然也有一个[漂亮的涡轮机翼收藏](http://chaaawa.com/airfoils/wind.html)。

如果你的需求不是很奇特，你只是想要阻力更小的东西，你也可以考虑【ErroneousBosch】的[非常简单的翼型发电机](https://github.com/ErroneousBosch/OpenSCAD_airfoil)，也是为了 OpenSCAD。制作一个 120 毫米宽 250 毫米长的 NACA 型机翼就像`airfoil_simple_wing([120, 0030], wing_length=250);`一样简单

如果你有更复杂的需求，或者想自己设计箔片，你总是可以画出点，转换成 DXF 和挤压。事实上，如果我们不在 OpenSCAD 中建模，我们就会这么做。但是谁愿意做那些体力劳动呢？

在开源模拟器、建模工具和 3D 可打印部件之间，如今没有理由低于标准的空气动力学。如果你打算[制造一个风力涡轮机](https://hackaday.com/2020/08/07/hawt-wind-turbine-is-mostly-3d-printed/)，那就好好做！(在评论中说出你最喜欢的空气动力学设计工具。我们在市场上。)