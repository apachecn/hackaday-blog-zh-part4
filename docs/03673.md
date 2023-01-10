# 手势控制的毁灭

> 原文：<https://hackaday.com/2019/07/22/gesture-controlled-doom/>

《毁灭战士》将作为整个 FPS 类型的创始游戏之一被永远铭记。它也是一款长期以来一直是黑客和修改者的沃土的游戏。[【Nick Bild】出于机器学习的考虑，决定将手势控制引入 iD 的经典射击游戏。](https://github.com/nickbild/doom_air)

该设置包括一台装有摄像头的 Jetson Nano，它可以拍摄玩家，并使用卷积神经网络来识别玩家的各种手势。一旦被识别，一个 API 请求被发送到一台笔记本电脑上，模拟相关的击键。这台笔记本电脑连接到一个投影仪上，创造了一个大屏幕，让疯狂打手势的玩家更容易跟上动作。

神经网络在 3300 张图片上接受训练——每个手势 300 张。[Nick]发现，使用更大的数据集实际上表现不佳，因为他在可靠地执行手势方面变得不那么勤奋。这表明培训网络的质量和数量一样重要。

有报道称，该网络相当可靠，看起来运转良好。不幸的是，可玩性受到限制，因为不可能一次手势操作多个按键。不过总的来说，它是如何用 CNN 进行手势识别的一个很好的例子。

如果你不相信这个演示，你可能会有兴趣了解一下[神经网络也可以用来给西红柿](https://hackaday.com/2018/04/26/neural-network-names-nightshades/)命名。如果你不想自己滚动姿势检测，可以看看这个使用 [CMU 的 OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose) 库的[自拍无人机](https://hackaday.com/2019/06/30/build-your-own-selfie-drone-with-computer-vision/)。休息后的视频。

 [https://www.youtube.com/embed/b2sixeEpBuU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/b2sixeEpBuU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

