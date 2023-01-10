# 神经网络知道猫什么时候想出去

> 原文：<https://hackaday.com/2018/12/21/neural-network-knows-when-cat-wants-to-go-outside/>

神经网络是一种计算机系统，它受到动物大脑结构的模糊启发，很像人脑，可以被训练成服从全能的家猫的突发奇想。[EdjeElectronics]已经建立了这样一个系统，他的猫因此过得更好。

这个建筑使用了一个装有 Pi 相机板的树莓 Pi 来拍摄房子后门周围的区域。Python 脚本定期捕捉图像，并将其传递给 TensorFlow 神经网络进行对象识别。TensorFlow 网络将对象类型和位置返回给 Python 脚本。该信息可以用于确定帧中是否有猫，以及它是在内部还是外部。如果猫连续十帧保持在某个位置，就会通过 Twilio 发送一条短信，指示主人让猫进来或出去，视情况而定。

三十年前，物体分类是一项不切实际的技术，但现在你可以在一台 30 美元的电脑上运行它，找出你的宠物在哪里。我们生活在一个怎样的时代！这个问题的类似解决方案可能是通过面部识别解锁的猫门。休息后的视频。

【感谢 Baldpower 的提示！]

 [https://www.youtube.com/embed/gGqVNuYol6o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gGqVNuYol6o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

