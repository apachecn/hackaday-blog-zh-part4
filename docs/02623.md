# 利用开放式摄影测量获得出色的 3D 扫描

> 原文：<https://hackaday.com/2019/04/07/get-great-3d-scans-with-open-photogrammetry/>

不久前，摄影测量学——将从不同角度拍摄的多张照片拼接成一个 3D 整体的过程——还是一件难事。如今，这很容易。Prusa Printers 的[Mikolas Zuza]有一个[指南，展示最先进的开源软件](https://www.prusaprinters.org/photogrammetry-2-3d-scanning-simpler-better-than-ever/)，它不仅更强大，而且更容易使用。他们还制作了一个视频，我们把它放在了下面。

基本上，这是一个使用[网络空间](https://alicevision.github.io/#meshroom)的指南，它基于 [AliceVision](https://alicevision.github.io/) 摄影测量框架。AliceVision 是一个研究平台，所以它有*巨大的*能力，但不一定关注用户体验。进入 Meshroom，它使这种力量变得可及。

Meshroom 做了各种各样很酷的把戏，比如向你展示当你向数据集添加更多图像时，3D 重建是什么样子的，这样你就知道在哪里拍摄下一张照片来填充不完整的补丁。它还可以从视频中重建，比如说，如果你只是在摄像机运行的情况下绕着物体走了一圈。

最终的渲染是计算密集型的，但 AliceVision 很好地利用了 Nvidia 显卡上的 CUDA，所以如果你有合适的硬件，你可以将通宵渲染缩短到几个小时。但是，即使你不得不等待结果，他们真的令人印象深刻。最棒的是，你只需用口袋里的手机就可以开始建立你的 3D 模型库。

如果你想知道如何使用摄影测量学中的模型，可以看看[Eric Strebel]的视频。如果这些高科技软件对你来说太难了，试试[基于牛奶的 3D 扫描仪](https://hackaday.com/2016/04/16/milk-based-3d-scanner/)。

 [https://www.youtube.com/embed/1D0EhSi-vvc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1D0EhSi-vvc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

