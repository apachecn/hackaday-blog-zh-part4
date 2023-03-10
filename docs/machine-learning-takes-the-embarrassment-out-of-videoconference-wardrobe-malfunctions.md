# 机器学习让视频会议衣柜故障不再尴尬

> 原文：<https://hackaday.com/2020/06/03/machine-learning-takes-the-embarrassment-out-of-videoconference-wardrobe-malfunctions/>

远程工作者:厌倦了只穿内衣出席视频会议的尴尬吗？用 [Safe Meeting](https://github.com/nickbild/safe_meeting) 来拯救屈辱和所有那些讨厌的去人力资源部门的旅行，如果你忘记了休闲星期五不应该是*那么*休闲，这个新系统会使用人工智能的力量来关闭你的相机。

下面的商业信息片是由[Nick Bild]带给你的，他说整个事情是开玩笑的，但我们在这里感觉到了某种程度的“需要是发明之母”。的确，突然涌入的远程工作新手肯定会增加视频会议事故的几率以及随之而来的尴尬，所以无论动力是什么，安全会议似乎都是一个好主意。它使用一个连接到 Jetson Nano 的 Pi 摄像头在视频会议期间捕捉你的图像，视频会议通过另一个摄像头进行。该流由卷积神经网络(CNN)进行分类，从而确定它是否可以看到你的内衣。如果可以，它会调用 REST API 来关闭摄像头。下面的视频展示了它的作用，它足够快地浇灭了摄像机，让你不再谦虚。

一想到[尼克]是如何开发出一套内衣专用训练集的，我们就不寒而栗，但我们为他这样做并为机器学习提供一个整洁的应用程序而鼓掌。他最近在这个领域做了一些有趣的工作，从[监测表面被触摸的地方](https://hackaday.com/2020/04/07/machine-vision-keeps-track-of-grubby-hands/)到[基于 6502 的手势识别系统](https://hackaday.com/2020/04/22/machine-learning-algorithm-runs-on-a-breadboard-6502/)。

 [https://www.youtube.com/embed/MeiassI3EQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MeiassI3EQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

