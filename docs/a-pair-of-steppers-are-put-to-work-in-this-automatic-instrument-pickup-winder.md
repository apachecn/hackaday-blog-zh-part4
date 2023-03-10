# 一对步进器在这个自动乐器拾取绕线机中工作

> 原文：<https://hackaday.com/2020/12/13/a-pair-of-steppers-are-put-to-work-in-this-automatic-instrument-pickup-winder/>

对于一些基本上是围绕一些磁极片的线圈的东西来说，电吉他拾音器是一项复杂的技术。乐器的音色在很大程度上取决于拾音器的卷绕方式，因此控制卷绕过程最好由机器来完成。这台自动捡拾络筒机并不是一台高端机器，但对于手头的工作来说已经足够了，并且有一些有趣的改进可能性。

首先，正如[混合信号]指出的那样，他的拾音器不是用来弹吉他的。[正如我们在](https://hackaday.com/2020/08/24/midi-slide-whistle-shows-the-value-of-a-proper-fipple/)之前看到的，他处理的音乐项目有些另类，这个单刀拾音器注定是另一种不寻常的乐器。当然，这并不是说吉他拾音器不能缠绕在这台机器上，感应器、螺线管或特斯拉线圈也可以。行走机构围绕两个 NEMA-17 步进电机构建，一个用于线圈轴，一个用于卷绕架。托架在一个短的 Acme 丝杠和直线轴承上运行，来回移动以或多或少均匀地缠绕线圈。一个顶部带有 CNC 护罩的 Arduino 运行该节目，允许走开线圈缠绕。

我们确实注意到线圈导线似乎在线圈架的末端聚集在一起。我们想知道这是否可以通过在接近线轴末端时加快托架电机的速度来解决，以便将线间距分散开一点。像这样的构建的好处是可以轻松地进行更改——归根结底，它只是代码。

 [https://www.youtube.com/embed/_2iHD2RhGzs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_2iHD2RhGzs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

