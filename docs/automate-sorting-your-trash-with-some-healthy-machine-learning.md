# 用一些健康的机器学习来自动分类你的垃圾

> 原文：<https://hackaday.com/2019/09/01/automate-sorting-your-trash-with-some-healthy-machine-learning/>

将垃圾分类成正确的类别几乎是每天都要做的事情。谁没有站在两个、三个、五个或更多的垃圾箱前(取决于你所在的地区和国家)，思考它应该进入哪个垃圾箱？[阿尔瓦罗·费伦·希福恩特斯]的[分离机器人项目](http://www.alvaroferran.com/projects/separaitor)是一个概念验证机器人，它使用机器人分类托盘和摄像头设置，旨在识别和分类放入分类托盘的垃圾。

硬件包括安装在蓝牙连接的平移和倾斜平台顶部的分类托盘。该平台与系统的其余部分进行通信，后者使用一个摄像头和 OpenCV 来获取图像数据，以及一个基于 [Keras 的](https://en.wikipedia.org/wiki/Keras)后端，后者用 Python 实现了一个深度学习神经网络。

该系统的训练是通过使用需要分类的物品的自制照片来进行的，因为这些照片最接近真实生活条件。在获得足够好的识别结果后，该系统被组装起来，并添加了运动检测功能，以便在新物品被扔进托盘时做出反应。然后，系统将尝试识别该物品，对其进行分类，并指示平台旋转到正确的方向，然后将其倾斜并放入适当的箱子中。休息后，观看嵌入式视频，了解系统的运行情况。

信不信由你，[这并不是第一个给 Hackaday](https://hackaday.com/2019/04/13/this-bot-might-be-the-way-to-save-recycling/) 增光添彩的垃圾分类机器人。像这样依赖于自动化和机器视觉的潜在概念，有一天可能会大规模部署，以帮助减少垃圾填埋场中的可回收材料。

 [https://www.youtube.com/embed/oepjfOC9nr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oepjfOC9nr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

