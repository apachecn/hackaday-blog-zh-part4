# 一种无人工智能的拍摄野生动物的方法

> 原文：<https://hackaday.com/2021/03/29/an-ai-free-way-to-catch-wildlife-on-camera/>

从这些天我们的新闻报道中“人工智能”一词的过度出现来看，我们显然正处于人工智能炒作周期的指数阶段，并且非常接近可怕的“膨胀预期的峰值”。似乎没有什么是人工智能做不到的，也没有什么是它的原则不能被应用于良性的——和有利可图的——效果。

我们不否认人工智能有巨大的潜力，但我们强烈怀疑很快会有一天，人们会对另一个本可以用更简单的方法解决的人工智能应用感到惊讶。一个更简单的方法的例子可以在[这个非人工智能的野生动物照片陷阱](https://there.oughta.be/a/photo-trap)中看到，它是由【Sebastian】拼凑起来的，用来捕捉一些害怕拍照的松鼠的照片。他没有用千兆字节的松鼠图像来训练人工智能，而是依赖于他的旧索尼 Alpha 相机，它有内置 WiFi。一个 Python 脚本连接到相机，相机在一个馈电盒上训练，并设置为非常窄的景深。这使得很大一部分场景无法聚焦，直到松鼠或其他动物来寻找食物。该脚本使用 OpenCV 中的拉普拉斯算子来检测现在对焦的场景的增加区域，并触发相机快门。[Sebastian]最后用这个方案拍了一些害羞的松鼠的精彩照片；下面的视频更详细地描述了设置。

当然，这不是我们第一次看到[拉普拉斯变换用于测量图像清晰度](https://hackaday.com/2018/07/13/replace-your-calipers-with-a-microscope-and-image-analysis/)，但是我们真的很喜欢【Sebastian】在这里采用的简单方法。松鼠也很可爱。

 [https://www.youtube.com/embed/JsOXjjVqZS0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JsOXjjVqZS0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

