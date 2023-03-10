# 机器人皮肤可以看到你何时(以及如何)触摸它

> 原文：<https://hackaday.com/2019/11/25/robotic-skin-sees-when-and-how-youre-touching-it/>

摄像头越来越不显眼了。现在他们藏在机器人的皮肤下。

来自瑞士苏黎世联邦理工学院的一组研究人员最近创造了一种[多摄像头光学触觉传感器](https://arxiv.org/abs/1910.14526)，它能够根据接触力的分布来监控周围的空间。该传感器使用一个堆叠，包括一个摄像头，发光二极管和三层硅胶，以光学方式检测皮肤的任何干扰。

![](img/8cf97cd076e8031bd92e0783fe49d8e3.png)

该方案是模块化的，在本例中使用四个摄像头，但可以从那里按比例放大。在制造过程中，放置相机和 LED 电路板，并浇注一层厚约 5 毫米的坚固硅胶。接下来，在浇注最终的 1.5 mm 黑色硅树脂层之前，浇注掺杂有球形颗粒的 2 mm 层。相机在粒子移动时跟踪它们，并使用这些信息来推断材料的变形和施加到其上的力。传感器还能够重建引起变形的力，并产生接触力分布。该演示使用了相当便宜的相机——由 NVIDIA Jetson Nano 开发套件监控的 Raspberry Pi 相机——总共提供约 65，000 像素的分辨率。

除了提供更多关于施加到表面的力的信息，该传感器还具有更大的接触面，并且比其他基于相机的系统更薄，因为它不需要使用反射组件。它会根据一个卷积神经网络定期重新校准自己，该网络使用来自三个摄像头的数据进行预训练，并使用来自所有四个摄像头的数据进行更新。未来可能的应用包括软机器人，在计算机视觉算法的帮助下改善基于触摸的传感。

虽然具有自我意识的机器人皮肤可能不会很快上市，但这无疑为机器人提供了一种可能性，即当太多的力施加在它们的结构上时，机器人可以检测到——这种机器相当于疼痛的感觉。

 [https://www.youtube.com/embed/lbavqAlKl98?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lbavqAlKl98?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Qes 的提示！]