# Adobe 神经网络检测 Photoshop 的恶作剧

> 原文：<https://hackaday.com/2019/06/18/adobe-neural-net-detects-photoshop-shenanigans/>

Photoshop 可以把不好的照片拍出来，让它看起来更好看。但它也能拍下你微笑的照片，并把它变成你皱眉的照片。篡改图像和视频当然是良性的，但也可能有邪恶的目的。Adobe 与伯克利的研究人员合作，看看他们能否教会计算机检测一种非常特殊的照片处理类型。事实证明，[他们可以](https://theblog.adobe.com/adobe-research-and-uc-berkeley-detecting-facial-manipulations-in-adobe-photoshop/)。

使用 Photoshop 的人脸识别液化功能，略多于一半的被测试者可以分辨出哪张照片是原始的，哪张是经过修饰以改变面部表情的。然而，经过充分的训练后，Adobe 的神经网络可以在 99%的情况下正确解决这个难题。

专注于特定类型的编辑可能看起来很奇怪，但它对于对一个人的面部进行非常微妙的改变是有用的。早期的研究致力于检测[原油处理](https://theblog.adobe.com/spotting-image-manipulation-ai/)。

听起来好像神经网络可以确定两张照片中的哪一张被修改了。这似乎是一个简单的问题，而不是简单地在没有其他照片进行比较的情况下识别一张被修改的照片。那会有用得多，但也可能困难得多。

我们认为神经网络检测假照片并不比让它们来评判我们的摄影作品更奇怪。我们甚至看到它们对[景深](https://hackaday.com/2018/12/11/improving-depth-of-field-with-only-5-phones/)进行了校正。