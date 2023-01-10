# 窥视亚马逊的最新网点

> 原文：<https://hackaday.com/2019/07/29/taking-a-peek-inside-amazons-latest-dot/>

像一百万左右的其他人一样，[Brian Dorey]在几周前亚马逊的大减价期间买了一个第三代 Echo Dot。价格不到正常零售价的一半，他认为这是探索亚马逊语音助手产品的最佳时机。但是低廉的价格也意味着他为了我们的视觉享受而把它撕成碎片的感觉并没有那么糟糕。

几乎所有人都认为，就企业补贴的家庭间谍设备而言，Echo Dot line 一直是一个相当可靠的表演者。它们很小，相当便宜，并提供大多数人期望的基本功能。虽然 Dot 的早期版本没有什么明显的*错误*,但亚马逊使用了这款设备的最新版本，给这款设备带来了更“高级”的外观和感觉。他们还试图从冰球大小的设备中挤出一点更好的音频。但是当然，一些未记录的变更也设法混入其中。

首先，最新版本的 Dot 删除了 USB 端口。[黑客曾使用早期版本硬件上的 USB 端口](https://medium.com/@micaksica/exploring-the-amazon-echo-dot-part-2-into-mediatek-utility-hell-b452f62e5e87)试图访问隐藏在其中的 Android(或者至少是亚马逊版本的 Android)操作系统，所以这是一个不幸的发展。另一方面，[Brian]报告说在设备底部有某种类型的调试头。一个类似的功能[允许黑客进入亚马逊的其他一些语音助手](https://hackaday.com/2017/08/03/the-amazon-echo-as-a-listening-device/)，所以我们建议乐观一点，直到被告知不是这样。

Echo Dot 采用四核联发科 MT8516BAAA 64 位 ARM Cortex-A35 处理器，操作系统采用 8GB 三星 KMFN60012M-B214 eMMC。一对德州仪器 LV320ADC3101 ADCs 用于处理来自 PCB 边缘四个麦克风的输入音频，[Brian]表示，当用户想要一点隐私时，似乎有一个飞兆 74LCX74 触发器可以切断音频馈送。

当然，最大的变化是在外部。新的 Dot 比以前的版本大得多，这意味着[如果他们想与亚马逊最新最棒的](https://hackaday.com/2018/03/11/gramazon-gives-your-echo-dot-a-1920s-makeover/)兼容，我们为其前身看到的所有令人敬畏的外壳都需要[重新制作。](https://hackaday.com/2017/10/16/echo-dot-finds-swanky-new-home-in-art-deco-speaker/)