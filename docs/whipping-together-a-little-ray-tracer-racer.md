# 组装一个小型光线追踪赛车

> 原文：<https://hackaday.com/2021/12/27/whipping-together-a-little-ray-tracer-racer/>

当你听到光线追踪时，你可能会想到复杂的黑暗算法，盯着它们的源代码太久会招致疯狂的开始。从技术上来说，你离真相不远了，但是[h3r2tic]在 GitHub 上放了一个[小型开源光线追踪游戏演示。驱动游戏的实际 rust 代码相对较短(只有四个文件)，最长的文件是物理文件。但是，当然，在这个示例中有一小部分代码是以库的形式存在的。](https://github.com/h3r2tic/cornell-mcray)

卡吉亚、 [physx-rs](https://github.com/EmbarkStudios/physx-rs) 和 [dolly](https://github.com/h3r2tic/dolly) 这三个库使得这个小演示成为可能。尤其是 Kajiya，它使用了较新的 RTX 特性(因此只支持较新的 Nvidia 和 AMD 卡)和 Vulkan 绑定，使得光线跟踪成为可能。但是，当然，它并不完全是光线追踪的，因为我们距离真正的实时光线追踪还有几年的时间。然而，光线追踪和传统栅格化的混合看起来令人难以置信。这个简单的小样本最重要的不是游戏本身，而是它代表了什么。它展示了创建这样一个样本是多么容易。即使仅仅五年，创造这样一个演示也需要巨大的努力和专业知识。

视觉上，看着就惊艳。虽然反射是最明显的，但从中获得的是实时全局照明带来的便利。快速浏览一下代码，可以发现场景中的灯光很少，尽管看起来光线很好，但阴影很柔和。传统的视频游戏花费大量的开发时间来照明场景，放置额外的灯光，并调整它们以弥补照明在光栅化环境中必须采取的所有捷径。随着越来越多的游戏是在脑海中建立光线跟踪，而不是在最后添加，我们可以放弃我们在今天的游戏中被迫使用的小崩溃的黑客山，只依靠光线来准确照亮场景。

如果使用一个库来进行光线追踪似乎太容易了，也许[你想在 excel](https://hackaday.com/2021/09/28/excel-ray-tracing-with-help-from-c/) 中接受光线追踪的挑战。休息后的视频。

 [https://www.youtube.com/embed/2KoLm8ajfo8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2KoLm8ajfo8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

