# 激光杀死一米外的蟑螂

> 原文：<https://hackaday.com/2022/10/03/laser-zaps-cockroaches-over-one-meter/>

你可能错过了本月的《东方昆虫》，爱丁堡赫瑞瓦特大学的一个项目引起了我们的注意。[Ildar]带领一组研究人员开发了一种由人工智能控制的激光，可以在 1.2 米的距离内压制移动的蟑螂。注意到使用化学杀虫剂控制害虫的各种问题，他的团队找到了一种非常规的方法。

害虫控制器的核心是一个 Jetson Nano，它使用 OpenCV 和 Yolo 对象检测来发现蟑螂和电流计来控制激光束。测试中使用了三种不同的激光，允许团队评估一系列波长、功率水平和光斑大小。不出所料，功率更高的 1.6 W 激光器效率更高、速度更快。

该项目在 GitHub 上([此处](https://github.com/Ildaron/Laser_control))，蟑螂机器学习图像集在[此处](https://www.kaggle.com/datasets/ildaron/tracking-a-cockroach-at-home)可用。但是[伊尔达]在报告的结论中指出，这是危险的。它适用于学术研究，但还不能用于一般用途，缺乏任何安全功能。这篇报道充斥着蟑螂的琐事，比如一只蟑螂的平均速度是 4.8 km/h，被电击时它们跑得快得多。如果你想自己用蟑螂做实验，可以链接到一家出售德国*蟑螂的宠物店，这也是这篇报道的目标。*

如果这个项目听起来很熟悉，那是因为它是我们去年写的前一个项目的改进。

 [https://www.youtube.com/embed/uHbCAFOaPhI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uHbCAFOaPhI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

