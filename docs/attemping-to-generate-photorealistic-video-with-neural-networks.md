# 用神经网络生成真实感视频的尝试

> 原文：<https://hackaday.com/2020/10/17/attemping-to-generate-photorealistic-video-with-neural-networks/>

在过去的十年里，我们看到了人工智能和神经网络领域取得的巨大进步。经过适当的训练，它们可以产生令人印象深刻的输出，无论是文本、图像还是简单的物体分类。将它们推到规定的运营区域之外也很有趣，就像乔恩·沃里克最近尝试的那样。

[Jon]的工作开始使用 NVIDIA 的 GauGAN 工具。它能够从分割地图中生成伪真实感的风景图像，其中 2D 图像的不同颜色代表树木、泥土、山脉或水等事物。在花了很多时间摆弄这个软件后，[Jon]决定看看它是否能被用于制作视频。

GauGAN 工具只能接收单个分割图，并输出单个图像，因此[Jon]必须发挥创意。进行了实验，其中视频被生成并作为单独的帧输出，这些帧作为单独的分割图被馈送给 GauGAN。来自 GauGAN 的输出帧被重新组合成一个视频。

正如人们所料，结果有些迷幻。GauGAN 的单一图像工作流程意味着连续帧之间只有巧合的相关性，创造了一个野生的，变化的面貌。虽然我们并不期望这种技术很快就能被用于严肃的目的，但这是一个很好的实验，可以看看这项技术能发展到什么程度。[我们也不是第一次看到这种技术被用于制作全动态视频](https://hackaday.com/2020/05/29/creating-surreal-short-films-from-machine-learning/)。休息后的视频。

 [https://www.youtube.com/embed/ZXFmZsv0Ddw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZXFmZsv0Ddw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

