# 可佩戴的静音锥保护你免受窃听

> 原文：<https://hackaday.com/2020/02/17/wearable-cone-of-silence-protects-you-from-prying-ears/>

小心，隔墙有耳。或者更具体地说，桌子上的智能扬声器有耳朵，你口袋里的手机，你手腕上的健身带，可能是电视，冰箱，烤面包机，甚至可能是马桶。哦，你的车也在听你的。大概吧。

一个人如何应对如此多的监听设备？或许[这款可穿戴智能设备音频干扰器](http://sandlab.cs.uchicago.edu/jammer/)可以解决这个问题。我们周围的 MEMS 麦克风都容易受到超声波的干扰，因为它们对超声波信号的响应是非线性的。其结果是，当 MEMS 听到超声波时，它会在频谱的可听部分产生一个宽带信号。这会产生静电噪音，有效地淹没麦克风可能拾取的任何其他声音。

为什么是可穿戴设备？诚然，来自芝加哥大学的 Yuxin Chin 和他的同事们可能用他们的原型扩展了这个术语的定义，但事实证明，移动干扰器比静态干扰器在阻挡声音方面做得更好。手镯式干扰器布满了超声波传感器，这些传感器发射重叠的场，并产生建设性和破坏性的干扰区域；佩戴者的动作改变了产生的死点的位置，提高了干扰效果。[他们的论文](http://people.cs.uchicago.edu/~ravenben/publications/pdf/ultra-chi20.pdf) (PDF 链接)有更深入的细节，而[GitHub 库](https://github.com/y-x-c/wearable-microphone-jamming)有你需要的一切。

我们在之前看到过[有点像这样的东西，但是那个建筑使用了白噪声进行掩蔽，并被贴在智能扬声器上。我们对可穿戴设备很感兴趣，特别是因为他们已经证明它在衣服下面很有效。超声波对 MEMS 麦克风的影响非常有趣。](https://hackaday.com/2019/01/17/win-back-some-privacy-with-a-cone-of-silence-for-your-smart-speaker/)

 [https://www.youtube.com/embed/-43-4LfqiTA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-43-4LfqiTA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[艾萨克]的提示。