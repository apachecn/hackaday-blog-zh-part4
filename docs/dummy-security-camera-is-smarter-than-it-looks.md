# 虚拟安全摄像头比看起来要聪明

> 原文：<https://hackaday.com/2019/05/22/dummy-security-camera-is-smarter-than-it-looks/>

虚拟安全摄像头背后的想法是，当那些不怀好意的人认为他们正在被记录时，他们可能会三思而行。显然，一个真正的安全摄像头会更好，但有时这在经济上或后勤上是不可能的。诚然，它们并不总是很有说服力，但对于几块钱来说，希望它足以让坏人三思。

[![](img/f122bb821411666006562ce3ed99a255.png)](https://hackaday.com/wp-content/uploads/2019/05/dummycam_detail.jpg) 但是如果这个“假”相机除了挂在墙上好看之外还能做点什么呢？[Chris Chimienti]认为他可以通过添加一些电子设备来改进这个想法，如果检测到运动就会通知他。作为一个额外的奖励，任何意识到相机本身是假的潜在罪犯可能会有勇气，当通知开始发出时，他们可能会发现自己处于一个粗鲁的惊喜之中。

在休息后的视频中，[克里斯]真的花了很长时间带领观众拆卸虚拟摄像机。事实证明，这些东西看起来会成为优秀的项目附件；它们很容易拆开，里面除了空空的空间什么都没有，甚至还有一个集成的电池盒。仅此一点就可以成为一个有用的提示，为将来存档。

然后他继续解释他是如何给这个假相机增加一些智能的。在原来的“镜头”上，他安装了一个 PIR 传感器、一些白色 led、一个光传感器和原来闪烁的红色 LED。所有这些都被安装在一个非常光滑的 3D 印刷板上，完美地集成到相机的机身中。新的硬件连接到相机内安装类似的 Wemos D1 迷你。视频的其余部分介绍了软件设置的各个方面，这肯定会引起任何想过推出自己的物联网设备的人的兴趣。

这种类型的 PIR 传感器是黑客的最爱，我们已经看到[许多项目将它们用于各种创造性目的](https://hackaday.com/2019/01/05/super-simple-sensor-makes-dslr-camera-motion-sensitive/)。我们以前甚至见过它们[与 ESP8266 配对用于互联网连接的运动感应](https://hackaday.com/2018/07/19/a-super-simple-esp8266-iot-motion-sensor/)，尽管没有整洁的安全摄像头外壳。

 [https://www.youtube.com/embed/5Rnwl8F-Wl4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5Rnwl8F-Wl4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

