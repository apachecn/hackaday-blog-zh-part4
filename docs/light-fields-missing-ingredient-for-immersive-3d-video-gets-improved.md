# 光场:沉浸式 3D 视频的缺失成分得到改善

> 原文：<https://hackaday.com/2020/10/20/light-fields-missing-ingredient-for-immersive-3d-video-gets-improved/>

[![](img/b6ca198d21aaf515dc0dfb132949c13c.png)](https://hackaday.com/wp-content/uploads/2020/10/Light-field-camera-from-the-inside.png)

46 time-synchronized action cameras make up the guts of the capture device.

3D 视频内容有一个很大的局限性，这是一个很难解决的问题。由摄像机捕获的视频(即使是高分辨率和非常宽的视野)仍然从固定的角度将场景记录为平面。这带来的限制对任何在 VR 中观看 3D 视频(或“360°视频”)并以错误的方式移动头部的人来说都是熟悉的。在这些视频中，一个人可以随意环顾四周，但在此过程中不能改变头部的位置。换句话说，转动头部向上、向下、向左或向右看都可以。将头抬得更高、更低、更近、更远或向旁边移动？这些都没用。像试图偷窥一个物体，或者为了更好地观看而稍微向旁边移动这样的自然动作根本不起作用。

光场视频改变了这一点。它是使用类似上图中的设备捕获的，谷歌有一个资源页面，提供了什么是光场视频，它看起来像什么，以及他们如何做的极好概述。该链接涵盖了他们的相机设备以及视频编码和渲染的最新改进，但也是一个很好的展示和讲述光场是什么以及它们能做什么的工具。

[![](img/d2cd3aa2005c3daf773879b66909ddbf.png)](https://hackaday.com/wp-content/uploads/2020/10/Dog-Light-field-Figure-8-optimized.gif)

Light field image, with viewer’s point of view moving in a figure eight pattern. Colors show depth layers interpolated by software.

元摄像机是一个直径不到一米的半球，包含 46 个指向外的时间同步动作摄像机阵列。在软件端，摄像机输入用于重建场景并创建一个 [6 DoF](https://en.wikipedia.org/wiki/Six_degrees_of_freedom) 的立体视频。换句话说，视频的视角根据用户移动他们的视点而正确地改变(无论如何，在非常粗略地对应于摄像设备的大小的区域内。)

另一个显著的改进是在结果视频的压缩和渲染方面。通过将视频减少到较小的固定数量的深度层来表示光场内容，可以利用传统的视频编码和压缩来提供可以在任何平台上轻松渲染的轻量级表示。一张图胜过千言万语，下面是一个展示光场图像的简短动画。视点以 8 字形移动，视角和视线完全按照人们的预期变化。动画还简要地窥视了窗帘后面，显示了软件用来决定什么属于哪里的颜色编码的深度层。

你可以[下载 SIGGRAPH 2020 技术论文的 PDF](https://augmentedperception.github.io/deepviewvideo/) ，或者[浏览 GitHub](https://augmentedperception.github.io/deepviewvideo/) 上托管的 DeepView 资源页面，获取大量浏览器内演示和可下载的 VR 耳机演示。该团队的视频演示也嵌入在下面，并提供了一个很好的概述。

 <https://storage.googleapis.com/immersive-lf-video-siggraph2020/DV_SIGG20_2020061701.mp4?_=1>

[https://storage.googleapis.com/immersive-lf-video-siggraph2020/DV_SIGG20_2020061701.mp4](https://storage.googleapis.com/immersive-lf-video-siggraph2020/DV_SIGG20_2020061701.mp4)

光场不一定是复杂的事务，有足够的空间让好奇的黑客去探索。感兴趣吗？ [[Alex Hornstein]在他的 2018 年 Hackaday 超级大会演讲中分享了一个关于光场工作的精彩演示](https://hackaday.com/2018/11/21/supercon-alex-hornsteins-adventures-in-hacking-the-lightfield/)，所以请查看一下。