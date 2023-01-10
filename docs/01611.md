# 一个受《星际迷航》启发的机器人，拥有树莓派和人工智能

> 原文：<https://hackaday.com/2018/12/21/a-star-trek-inspired-robot-with-raspberry-pi-and-ai/>

当[314Reactor]得到一个机器人汽车套件时，他知道他想给它添加一些额外的东西。几乎在同一时间，他正在看《星际迷航》中的一集，里面有 exo comp——在危险区域工作的机器人。他决定利用这些虚构的设备来激发他对汽车套件的修改。诚然，虚构的机器人很聪明，有一个复制器。所以你知道他不会做一个真正的工作复制品。不过话说回来，电视剧里的那些也没有那些。

Raspberry Pi 使用标准相机运行 Tensorflow。这使它能够识别感兴趣的对象(假设它能正确识别)，并将图像和一些识别信息一起发送回操作员。该套件已经有一个 Arduino 板载，新机器人通过串行端口与它交谈。你可以在下面看到一个关于这个项目的视频。

由于最初的套件使用蓝牙适配器来发送和接收来自移动设备的串行命令，所以设计有点复杂。然而，该套件的控制器软件允许额外的按钮，因此 Arduino 可以接收命令并将它们发送到 Pi。

这个机器人的代码被称为 Scorpion，可以在 GitHub 上找到。额外的命令与摄像机有关，也与一些移动钳子模仿电视机器人的伺服系统有关。图像通过电报云服务返回给运营商。

我们不得不承认，蝎子和 exocomp 不太一样。但是我们可以看到对设计的影响。它不够聪明，无法在镜子中识别自己，所以我们认为它没有感知能力。

我们之前见过[智能机器人使用 Tensorflow](https://hackaday.com/2016/10/09/tensorflow-robot-recognizes-objects/) 。如果你愿意，你可以试试 [OpenCV](https://hackaday.com/2014/08/24/open-source-marker-recognition-for-augmented-reality/) 。

 [https://www.youtube.com/embed/BOUb5kaAydw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BOUb5kaAydw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

