# 一个标签制造商使用人工智能真的很差

> 原文：<https://hackaday.com/2021/12/21/a-label-maker-that-uses-ai-really-poorly/>

[8BitsAndAByte]发现自己痴迷于给家里的物品贴标签，并且像世界上其他人一样，想看看有哪些简单的常规任务可以通过使用人工智能变得不必要的复杂。她认为将这项任务交给我们的人工智能统治者会很有趣，而不是使用人类智能来手动识别物体，结果非常有趣。

她构建了一个纸板外壳，其中包含一个树莓 Pi 3B+，Pi 相机模块 V2，以及一个用于制作标签的小型热敏打印机。外壳上有一个摄像头孔和一个拍照按钮。Pi 拍摄的图像由 DeepAI DenseCap API 进行分析，理论上，它应该为图像中检测到的每个对象创建一个标签。不幸的是，[它似乎没有做得很好](https://hackaday.com/2017/11/03/googles-inception-thinks-this-turtle-is-a-gun/)并且[8BitsAndAByte]留下了与她拍摄的任何对象都不匹配的标签。在某些情况下，它甚至没有接近，例如，模型认为苹果是一个人的头，旋转拨号电话是一个杯子。去想想。不过，这似乎并没有真的困扰她，她从整件事情中得到了相当好的笑声。

该模型似乎检测到图像中的所有对象，但只打印它最确定的对象的标签。所以也许她的部分问题是背景中有太多的物体？如果是这样的话，你可以通过在中性背景下放置物体来提高模型的准确性。这可能会减少人工智能的困惑，并可能给你更好的结果。或者尝试一个完全不同的分类器？或者不要。然后你可以在下次聚会时把它作为一个[的有趣的、令人作呕的项目。那也行得通。](https://hackaday.com/2016/12/24/simon-says-smile-human/)

很酷的项目[8BitsAndAByte]！嘿，也许这是一个信号，毕竟这个世界仍然需要一些人类智慧。谁知道呢？

 [https://www.youtube.com/embed/hlpnbiDAdCg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hlpnbiDAdCg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

