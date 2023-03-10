# 艺术项目快速而疯狂地将音频转化为视觉享受

> 原文：<https://hackaday.com/2021/10/14/art-project-fast-and-fouriously-transforms-audio-into-eye-candy/>

快速傅立叶变换。频谱分析仪。瀑布展示。不久前，这样的术语是为高端测试设备保留的。但是啊，事情发生了多么大的变化啊！对于许多黑客读者来说，随着现代微控制器变得越来越强大，并因此被赋予越来越强大的软件库，它们已经改变了这一场景，这并不奇怪。[mircemk]已经使用这样一个库以及其他开源软件，结合大多数现成的硬件，创建了他所谓的 [DIY FFT 频谱分析仪](https://hackaday.io/project/182080-diy-simple-fft-spectrum-analyzer)。这个巧妙的项目旨在取悦眼球，而不是作为一件测试设备。

整体构建相对简单。音频通过线路输入插孔或麦克风获取，然后通过管道传输到 ESP32。ESP32 通过 FFT 例程运行音频，将音频采样、切片并切割成 16 个单独的频段。视觉输出显示在 16 x 16 WS2812 Led 矩阵上。[mircemk]编写了几个例程来显示输入的音频，带有瀑布、图表和其他视觉效果，非常美观。其中一些是彻头彻尾的催眠！你可以在休息时间下面的视频中看到结果。

当然，这种构建不会停留在将一些硬件和一些无源组件拼凑在一起。要真正完成，它需要装在值得展示的东西里。[mircemk]没有让人失望，因为一个漂亮的 3D 打印外壳很好地包裹了这一切。

我们认为最终产品非常棒，它让我们想起了在我们黑客生涯早期启发我们的一些东西。我们希望看到这个项目与任何形式的互动音乐艺术装置相结合，越深奥越好。也许一个 [555 定时器合成器可以满足这个要求](https://hackaday.com/2015/02/07/modular-555-synth-is-controlled-by-midi/)？请务必通过提示热线与我们[分享您自己的黑客技术！](https://hackaday.com/submit-a-tip/)

 [https://www.youtube.com/embed/0flgNrmBseA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0flgNrmBseA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

