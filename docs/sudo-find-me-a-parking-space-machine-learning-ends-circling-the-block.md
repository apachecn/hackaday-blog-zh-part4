# Sudo 给我找个停车位；机器学习结束了

> 原文：<https://hackaday.com/2019/02/04/sudo-find-me-a-parking-space-machine-learning-ends-circling-the-block/>

如果你住在繁华的城市，有开车的人过来，他们可能很难找到停车位。也许*你*有一个指定的空间，但是他们听天由命，用鹰眼绕着街区转。考虑到这些朋友，[亚当·盖特基]写了一个 Python 脚本[，它从网络摄像头获取视频，并逐帧分析，以计算出街道停车位何时开放](https://medium.com/@ageitgey/snagging-parking-spaces-with-mask-r-cnn-and-python-955f2231c400)。当光荣的时刻到来时，他通过 Twilio 收到一条带有虚空图片的短信。

这听起来很复杂，但大部分工作已经完成。汽车是机器学习的热门目标，因此汽车的大型数据集已经存在。[Adam]也不需要训练神经网络——他找到了一个预先训练好的 Mask R-CNN 模型,其中有 80 种常见物体的数据，如人、动物和汽车。

该模型提供了许多有用的信息，包括每辆车的边界框和像素坐标。由于盒子是重叠的，需要有一种方法来确定空间中是否真的有一辆车，或者只是其他车的保险杠。[Adam]使用 union 上的交集来实现这一点，这可以作为 Mask R-CNN 模型库的一个功能方便地获得。该函数返回一个分数，所以只需要忽略低分数的边界框。

[亚当]故意让剧本适应。这里或那里的一些变化，你可以用机器人收集器捡起网球，或者马上分析你所在街区的人类迁移模式。或者把它换一下，[检测所有在你家附近跑停车标志的车](https://hackaday.com/2017/04/12/detect-cars-running-stop-signs-and-squirrels-running-across-the-roof/)。

谢谢你的提示，[foamyguy]。