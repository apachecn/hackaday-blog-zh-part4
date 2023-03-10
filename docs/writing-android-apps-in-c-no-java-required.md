# 用 C 编写 Android 应用程序，不需要 Java

> 原文：<https://hackaday.com/2020/05/13/writing-android-apps-in-c-no-java-required/>

旧的 Android 设备只需一首歌就能买到，而且在许多情况下仍然拥有相当大的计算能力。凭借内置网络、电池和大触摸屏，它们可以在许多应用中轻松取代树莓 Pi 和外部显示器。碰巧的是，谷歌使得开发你自己的安卓软件变得非常容易。只有一个问题:你必须用 Java 来做。

为了摆脱所有的臃肿和开销， [[CNLohr]着手研究如何让 100% C 代码在 Android 设备上运行](https://github.com/cnlohr/rawdrawandroid)。在从互联网最深处和最黑暗的角落收集信息和资源后，他发现这个过程其实并没有那么糟糕。他精心制作了一个 makefile，可以用来在几秒钟内启动并运行你自己的 C 程序。

我们指的是字面意思。正如休息后的视频所展示的，[CNLohr]能够用一条命令在不到两秒的时间内编译、上传和运行 C Android 程序。这种快速的开发周期允许您在实际完成工作上花费更多的时间，因为您可以像在本地机器上运行代码一样快速地迭代您的代码版本。

[CNLohr]说你仍然需要安装谷歌的 Android Studio，所以这并不像是一些洁净室实现。但是一旦安装好了，你就可以从他的 makefile 中调用任何东西，而不必直接与它交互。即使你对官方的 Android 开发工具没有任何问题，对于能够[编写一个不需要几兆字节](https://hackaday.com/2010/07/15/android-dev-101-%e2%80%93-part-1hello-world/)的“Hello World”来说，还是有一些东西可以说的。

 [https://www.youtube.com/embed/Cz_LvaN36Ag?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Cz_LvaN36Ag?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

