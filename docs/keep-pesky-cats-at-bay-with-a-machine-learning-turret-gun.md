# 用机器学习炮塔枪赶走讨厌的猫

> 原文：<https://hackaday.com/2019/07/12/keep-pesky-cats-at-bay-with-a-machine-learning-turret-gun/>

在你的生活中有了一只猫后，不需要多久你就会知道谁才是真正的主人。猫在它们想做的时候会做它们想做的事情，而且只要适合它们，它们就会一直做下去。任何与你的需要和需求相关的事情都是完全巧合的，并且会在没有通知的情况下改变，因为猫。

阿尔瓦罗·费伦·希福恩特斯(Alvaro ferrán Japan)几乎是吃了苦头才知道这一点的，当时他的猫养成了探索厨房工作台面的习惯，当他不在时，它差点打开了灶台。为了调整这种行为，[阿尔瓦罗]建造了[这种 AI Nerf 炮塔](http://www.alvaroferran.com/blog/feline-learning)。该系统的商业端只是一把枪，安装在由 3D 打印零件和一对业余爱好伺服系统制成的云台上。一个网络摄像头安装在枪的顶部，并输入到一台运行软件的电脑中，该软件实现了 YOLO3 定位算法。该程序找到猫，跟踪它的质心，并旋转枪来匹配它。如果猫在工作台面上方的禁区停留三秒钟，它就会在自己的大致方向上挨一镖。[阿尔瓦罗]发现追踪他的枪的噪音足以让猫蹦跶，证明猫只要适合自己，就有能力学习。

我们喜欢这种建筑，也欣赏任何试图让一只猫给一个家庭带来的混乱变得有序的尝试。这也让我们想起了[【马蒂亚斯·万德尔】最近试图在他的店里保暖](https://hackaday.com/2019/03/22/raspberry-pi-tracks-humans-blasts-them-with-heat-rays/)，尽管他的检测算法要简单得多。

 [https://www.youtube.com/embed/OXh9hrmX15k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OXh9hrmX15k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

