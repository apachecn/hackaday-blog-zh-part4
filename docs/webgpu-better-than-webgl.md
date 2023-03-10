# WebGPU…比 WebGL 好？

> 原文：<https://hackaday.com/2022/03/09/webgpu-better-than-webgl/>

随着浏览器变得更像一个操作系统，我们看到更多的深层功能被嵌入其中。例如，你现在可以为浏览器编写一种汇编语言。自 2011 年左右以来，复杂的图形一直在使用 WebGL，但有些人觉得很难使用。[苏尔马]是这些人中的一员，他尝试了一种新方法，这种方法只是表面上做同样的事情: [WebGPU](https://surma.dev/things/webgpu/) 。

[苏尔马]更喜欢它，并在帖子中分享了许多信息，奇怪的是，帖子不太使用 WebGPU 进行图形处理。相反，这篇文章专注于使用 GPU 核心进行快速计算，这是你可以用 WebGPU 做的其他事情。但是，如果你的目标是在屏幕上画画，你需要知道基本知识和链接到一个有这样做的例子的网站。

请记住，您可能需要做一些特殊的事情来打开浏览器中的 WebGPU 或切换浏览器。虽然 WebGL 是 OpenGL 的一个瘦包装器，但 WebGPU 是一个抽象，可以驱动 Vulkan、Metal 或 DirectX 12 所有与 GPU 对话的流行方式，具体取决于您的操作系统。

这篇文章很长，涵盖了着色器、管道和暂存缓冲区等主题。当然，这个 API 还处于草稿阶段，还不稳定，但是它看起来足够充实，你现在学到的东西将来可能也会有用。

我们已经在浏览器中看到了用来做[神经网络的 GPU 处理。你可能也会对查看](https://hackaday.com/2017/08/04/neural-nets-in-the-browser-why-not/) [GPU.js](https://hackaday.com/2017/07/17/using-the-gpu-from-javascript/) 感兴趣。